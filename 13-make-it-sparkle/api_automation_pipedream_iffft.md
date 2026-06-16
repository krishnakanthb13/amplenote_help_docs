# Connect Amplenote to other apps using Siri Shortcuts, IFTTT or Pipedream (custom API integrations & automations)

> [← Help Index](../00-index.md) · Category: [Make it Sparkle](./index.md) · [Source ↗](https://www.amplenote.com/help/api_automation_pipedream_iffft)

## What are automations and how are they useful?

Services like Siri Shortcuts, IFTTT and Pipedream allow you to connect Amplenote to other applications, enabling automation of repetitive tasks or integration of multiple app features.

The most common automation pattern uses "Trigger and Action" architecture: something happens in one app (trigger), prompting an action in another app. However, "Amplenote only registers Actions and no Triggers" currently.

**Note:** These are third-party services unrelated to Amplenote. Fees may apply based on automation frequency, though free functionality exists as of March 2023.

## How to create Siri Shortcuts with Amplenote Actions

1. Open Shortcuts app and click the `+` button to create a new Shortcut
2. Search for Amplenote or scroll to find it in your apps list
3. Select from available actions:

| Action | Function |
|--------|----------|
| Add to Daily Jots | Inserts input at top of daily jot as task/paragraph/bullet |
| Add to Notes | Inserts input at top of specified notes |
| Create Note | Creates new note with specified tags |
| Find Notes | Returns notes matching title query or tag selection |
| Get Formatting | Choose format (task/bullet/paragraph) programmatically |
| Get Notes | Select notes to pass to other Actions |
| Get Tags | Select tags to pass to other Actions |

For additional examples, see "Recording voice notes, speech-to-text or audio notes (OpenAi, Siri)".

### How to use Shortcuts?

Shortcuts connect different apps—for example, adding third-party content to Amplenote. Using "[Automations](https://support.apple.com/en-gb/guide/shortcuts/apd690170742/ios)", trigger Shortcuts automatically when events occur.

**Share your creations:** Contact support@amplenote.com to share Siri Shortcuts with other users.

## How to set up an IFTTT integration

1. Navigate to [https://ifttt.com/create](https://ifttt.com/create) or browse [published Applets](https://ifttt.com/amplenote)
2. Choose a trigger ("If This" step)—for example, "New file in your folder" from Google Drive
3. Configure trigger settings (log in, specify folder)
4. Select Amplenote as the action ("Then That" step)
5. Choose an action type (e.g., create task)
6. Configure parameters:
   - **Text:** Visible task contents
   - **Description:** Added as Rich Footnote
   - **Ingredients:** Fields automatically pulled from trigger (use "Add ingredient" button)
7. Click "Create Action" and enable the Applet

**Formatting tip:** Use `<br>` for line breaks to format text across multiple lines.

## How to set up a Pipedream integration

1. Create account and new workflow
2. Add trigger—for example, "Google Drive: New Files (Instant)"
3. Connect Google account and select drive folder
4. Click "Create Source" and trigger an event by creating a file in the chosen folder
5. Open the event, click the "more" button, and copy the `webViewLink` property path
6. Add an Amplenote step: select note and format nodes using JSON structure
7. Click "Test" button to verify success
8. Deploy your integration

**Node format example:**
```json
{
  "type": "check_list_item",
  "content": [{
    "type": "paragraph",
    "content": [{
      "type": "link",
      "attrs": {"href": "{{steps.trigger.event.webViewLink}}"},
      "content": [{"type": "text", "text": "New file from Google Drive"}]
    }]
  }]
}
```

For details, see [Amplenote's API docs](https://www.amplenote.com/api_documentation#post-/notes/-uuid-/actions).

## Pipedream usage examples

You can use Pipedream's default steps or custom code (Python/JavaScript) for automation. Common actions include:

### Example 1: Adding a simple task using the default Amplenote step

Use the "Create Task" step with this JSON:
```json
{
  "type": "check_list_item",
  "content": [{
    "type": "paragraph",
    "content": [{"type": "text", "text": "Remember to look at Google Drive today"}]
  }]
}
```

### Example 2: Adding something to the daily jots using custom Javascript code

For capturing data to today's Daily Jot without manual destination selection:

**Step 1 - Calculate today's date:**
```javascript
import { DateTime } from "luxon";
export default defineComponent({
  async run({ steps, $ }) {
    const last24Hours = Math.floor((Date.now() - 24 * 60 * 60 * 1000) / 1000);
    const dt = DateTime.local();
    let suffix;
    let j = dt.day % 10, k = dt.day % 100;
    if (j == 1 && k != 11) suffix = 'st';
    if (j == 2 && k != 12) suffix = 'nd';
    if (j == 3 && k != 13) suffix = 'rd';
    else suffix = 'th';
    let today = dt.setLocale('en-US').toLocaleString({month: 'long', day: 'numeric'});
    today = today + suffix + ', ' + dt.year;
    $.export('today', today);
    $.export('last24Hours', last24Hours);
  },
})
```

**Step 2 - Get or create today's jot:**
```javascript
import { axios } from "@pipedream/platform"
export default defineComponent({
  props: {
    amplenote: { type: "app", app: "amplenote" }
  },
  async run({steps, $}) {
    const headers = { "Authorization": `Bearer ${this.amplenote.$auth.oauth_access_token}` };
    const today = steps.calculate_todays_date.today;
    const last24Hours = steps.calculate_todays_date.last24Hours;
    const data = await axios($, {
      method: "GET",
      url: `https://api.amplenote.com/v4/notes?since=${last24Hours}`,
      headers: headers,
    })
    let note = getTodaysJot(data, today);
    if (typeof note === 'undefined') {
      const jsonData = {
        name: today,
        tags: [{ text: 'daily-jots', color: 'b4bfcc' }]
      }
      note = await axios($, {
        method: 'POST',
        data: jsonData,
        url: `https://api.amplenote.com/v4/notes`,
        headers: {
          Authorization: `Bearer ${this.amplenote.$auth.oauth_access_token}`,
        },
      })
    }
    $.export("Note UUID", note.uuid);
  }
})

function getTodaysJot(data, noteTitle) {
  const dailyJotsTag = data.tags['daily-jots'].text;
  const dailyJotsNote = data.notes.filter(note => {
    const noteTags = note.tags.map(tag => data.tags[tag].text);
    return noteTags.includes(dailyJotsTag) && note.name.includes(noteTitle);
  });
  return dailyJotsNote[0];
}
```

**Step 3 - Add task to daily jot:**
```javascript
import { axios } from "@pipedream/platform"
export default defineComponent({
  props: {
    amplenote: { type: "app", app: "amplenote" }
  },
  async run({steps, $}) {
    const uuid = steps.get_or_create_todays_jot["Note UUID"];
    const task = {
      type : "INSERT_NODES",
      nodes : [{
        type : "check_list_item",
        content : [{
          type :'paragraph',
          content :[{
            type : 'text',
            text : 'Remember to check your Google Drive!'
          }]
        }]
      }]
    }
    return await axios($, {
      method: 'POST',
      url: `https://api.amplenote.com/v4/notes/${uuid}/actions`,
      data: task,
      actions: 'INSERT_NODES',
      headers: {
        Authorization: `Bearer ${this.amplenote.$auth.oauth_access_token}`,
      },
    })
  },
})
```

### Example 3: Adding a task containing a link using the default Amplenote step

Use this JSON to add a task with an inline tag reference:
```json
{
  "type": "check_list_item",
  "content": [{
    "type": "paragraph",
    "content": [
      {"type": "text", "text": "Remember to check Drive Inbox "},
      {
        "type":"link",
        "attrs": {"href": "https://www.amplenote.com/notes/46cf1ec0-f63e-11ed-a472-269378144d6e"},
        "content": [{"type": "text", "text": "@home"}]
      }
    ]
  }]
}
```

### Example 4: Adding a task containing an inline tag using a custom Javascript step

**Step 1 - Get note UUIDs:**
```javascript
import { axios } from "@pipedream/platform"
export default defineComponent({
  props: {
    amplenote: { type: "app", app: "amplenote" }
  },
  async run({steps, $}) {
    const data = await axios($, {
      method: 'GET',
      url: `https://api.amplenote.com/v4/notes`,
      headers: {
        Authorization: `Bearer ${this.amplenote.$auth.oauth_access_token}`,
      },
    })
    const note = filterNote(data, 'Drive Inbox');
    const inlineTag = filterNote(data, '@home');
    $.export('Destination note UUID', note.uuid);
    $.export('inline tag UUID', inlineTag);
  },
})

function filterNote(data, title) {
  const [result] = data.notes.filter(note => {
    if (note.name.includes(title)) {
      console.log(`Note ${note.name} found`);
      console.log(note);
      return note;
    }
  })
  return result;
}
```

**Step 2 - Create task with inline link:**
```javascript
import { axios } from "@pipedream/platform"
export default defineComponent({
  props: {
    amplenote: { type: "app", app: "amplenote" }
  },
  async run({steps, $}) {
    const driveInbox = steps.get_task_with_inline_tag["Destination note UUID"];
    const inlineTag = steps.get_task_with_inline_tag["inline tag UUID"];
    const task = {
      type : "INSERT_NODES",
      nodes : [{
        type: 'check_list_item',
        content: [{
          type: 'paragraph',
          content: [
            { type: 'text', text: 'Remember to check the drive Inbox ' },
            {
              type: 'link',
              attrs: { href: `https://www.amplenote.com/notes/${inlineTag.uuid}` },
              content: [{ type: 'text', text: inlineTag.name }]
            }
          ]
        }]
      }]
    }
    return await axios($, {
      method: 'POST',
      url: `https://api.amplenote.com/v4/notes/${driveInbox}/actions`,
      data: task,
      actions: 'INSERT_NODES',
      headers: {
        Authorization: `Bearer ${this.amplenote.$auth.oauth_access_token}`,
      },
    })
  },
})
```

---

**Resources:**
- [Siri Shortcuts documentation](https://support.apple.com/en-gb/HT209055)
- [IFTTT Amplenote integration](https://ifttt.com/amplenote)
- [Pipedream platform](https://pipedream.com)
- [Amplenote API documentation](https://www.amplenote.com/api_documentation)
- [Luxon date library](https://moment.github.io/luxon/)
- [Axios HTTP client](https://axios-http.com/docs/intro)
- [Pipedream code steps guide](https://pipedream.com/docs/code/)
