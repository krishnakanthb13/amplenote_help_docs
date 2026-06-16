# Actions: Ways to invoke/initiate plugin execution

> [← Help Index](../00-index.md) · Category: [Plugins](./index.md) · [Source ↗](https://www.amplenote.com/help/developing_amplenote_plugins/actions)

Plugin actions define interaction points for how plugin code gets called. These actions can return values directly or as Promises, and each receives an App Interface object as the first argument.

## Optional Check Function

Each action can define a `check` function that determines whether the plugin displays to users in that context. It returns a boolean or Promise resolving to one, receiving the same arguments as the `run` function.

## Available Actions

### appOption
Adds app-wide options invokable from "jump to note" (web) or quick search (mobile) dialogs.

**Arguments:** `app` (App Interface)

### dailyJotOption
Adds suggestions below today's daily jot with a run button. Returns nothing; customize button text by returning a string from the `check` function.

**Arguments:** `app`, `noteHandle`

### eventOption
Adds options to popup menus for calendar events (tasks and scheduled bullets).

**Arguments:** `app`, `taskUUID` (String)

### imageOption
Adds options to image dropdown menus within notes.

**Arguments:** `app`, `image` (image object)

### insertText
Inserts text at specific note locations when using `{expression}` syntax.

**Returns:** String replacing the expression; customize the keyword via `check` function

### linkOption
Adds buttons to Rich Footnote popups when cursor is in a link.

**Arguments:** `app`, `link` (link object)

### linkTarget
Called when plugin links (`plugin://<plugin UUID>`) are clicked.

**Arguments:** `app`, optional query string from URL

### noteOption
Adds options to per-note menus when editing specific notes.

**Arguments:** `app`, `noteUUID` (String)

### onEmbedCall
Triggered when embed code calls `window.callAmplenotePlugin`.

**Arguments:** `app`, `...args` (serializable via JSON)

**Returns:** Any JSON-serializable value

### onNavigate
Called when users change locations (opening notes, jots, etc.) and on initial plugin load. Note: "the `check` function — if defined — will not be called for this action."

**Arguments:** `app`, `url` (String)

### onNoteCreated
Called when a note is created on the current client.

**Arguments:** `app`, `noteHandle`

### onPluginCall
Called when another plugin invokes `app.callPlugin` with this plugin's identifier.

**Arguments:** `app`, `sourcePlugin` (object with `uuid` and `source` keys), `...args`

### renderEmbed
Renders HTML for embeds in isolated iFrames with relaxed CSP rules.

**Arguments:** `app`, `...args` (from embed parameters)

**Returns:** String of HTML

#### Embed Features
- `<a>` tags with class `amplenote-link` navigate to Amplenote client locations
- Supports aspect ratio via `data-aspect-ratio` attribute
- Inline embeds accept parameters: `plugin://UUID?something=1&else=2`

#### Embed-to-Plugin Communication
Embeds call the controlling plugin using `window.callAmplenotePlugin()`, triggering the plugin's `onEmbedCall` action, which can return values back to the embed.

### replaceText
Replaces highlighted text via selection menu.

**Arguments:** `app`, `text` (String — selected text)

**Returns:** String (replacement text) or null (cancel replacement)

### suggestTaskTargetNotes
Suggests ordered notes where tasks could be added.

**Arguments:** `app`, `task`, `suggestedNoteHandles` (Array)

**Returns:** Array of noteHandle objects or UUID strings

### taskOption
Adds options to task commands menu (invoked via `!` in task body).

**Arguments:** `app`, `task`

### validateSettings
Validates plugin settings when saved, useful for API key verification.

**Arguments:** `app` (limited interface), `settings` (Object)

**Returns:** Array of error strings or falsy value indicating no problems
