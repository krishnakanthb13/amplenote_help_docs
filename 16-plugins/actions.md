# Actions: Ways to invoke/initiate plugin execution

> [← Help Index](../00-index.md) · Category: [Plugins](./index.md) · [Source ↗](https://www.amplenote.com/help/developing_amplenote_plugins/actions)

Plugin actions define interaction points for how plugin code gets called. These actions can return values directly or as Promises, and each receives an App Interface object as the first argument.

## Optional Check Function

Each action can define a `check` function that determines whether the plugin displays to users in that context. It returns a boolean or Promise resolving to one, receiving the same arguments as the `run` function.

## Available Actions

### appOption
Adds app-wide options invokable from "jump to note" (web) or quick search (mobile) dialogs.

**Arguments:** `app` (App Interface)

![appOption app-wide option example](https://images.amplenote.com/fae505fa-bd40-11ed-8e3b-9a67e5fef0db/188f9755-da0e-470e-8d40-e111f45d1cdf.png)

### dailyJotOption
Adds suggestions below today's daily jot with a run button. Returns nothing; customize button text by returning a string from the `check` function.

**Arguments:** `app`, `noteHandle`

![dailyJotOption suggestion below the daily jot](https://images.amplenote.com/fae505fa-bd40-11ed-8e3b-9a67e5fef0db/9da23331-2073-4ce7-8a01-0c515697142f.png)

![dailyJotOption with customized button text](https://images.amplenote.com/fae505fa-bd40-11ed-8e3b-9a67e5fef0db/d0d1f3ba-14bd-40cc-93c4-126473b31d01.png)

### eventOption
Adds options to popup menus for calendar events (tasks and scheduled bullets).

**Arguments:** `app`, `taskUUID` (String)

### imageOption
Adds options to image dropdown menus within notes.

**Arguments:** `app`, `image` (image object)

![imageOption in an image dropdown menu](https://images.amplenote.com/fae505fa-bd40-11ed-8e3b-9a67e5fef0db/99427c5b-e917-4372-b2e9-47d76ce75ae5.png)

### insertText
Inserts text at specific note locations when using `{expression}` syntax.

**Returns:** String replacing the expression; customize the keyword via `check` function

![insertText auto-complete menu](https://images.amplenote.com/2ae961e0-bc5d-11ed-808b-e21efa2d8566/011fd085-edee-4650-a24c-97278fcac158.png)

![insertText with a custom keyword](https://images.amplenote.com/fae505fa-bd40-11ed-8e3b-9a67e5fef0db/5001d613-ce83-4508-8040-e6bbba13ede1.png)

### linkOption
Adds buttons to Rich Footnote popups when cursor is in a link.

**Arguments:** `app`, `link` (link object)

![linkOption button in a Rich Footnote popup](https://images.amplenote.com/fae505fa-bd40-11ed-8e3b-9a67e5fef0db/deac9f00-e496-4420-a0b0-8397a29bc87b.png)

### linkTarget
Called when plugin links (`plugin://<plugin UUID>`) are clicked.

**Arguments:** `app`, optional query string from URL

![linkTarget plugin link example](https://images.amplenote.com/fae505fa-bd40-11ed-8e3b-9a67e5fef0db/6aba51ee-90a7-436a-bdc1-214a8fb26af7.png)

### noteOption
Adds options to per-note menus when editing specific notes.

**Arguments:** `app`, `noteUUID` (String)

![noteOption in a per-note menu](https://images.amplenote.com/2ae961e0-bc5d-11ed-808b-e21efa2d8566/3ae0c6a7-1147-4453-afe9-303eb00613fb.png)

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

![renderEmbed rendered embed example](https://images.amplenote.com/fae505fa-bd40-11ed-8e3b-9a67e5fef0db/8dcb94e1-ca68-4c9f-af6e-a34708c1fb03.png)

#### Embed Features
- `<a>` tags with class `amplenote-link` navigate to Amplenote client locations
- Supports aspect ratio via `data-aspect-ratio` attribute
- Inline embeds accept parameters: `plugin://UUID?something=1&else=2`

#### Embed-to-Plugin Communication
Embeds call the controlling plugin using `window.callAmplenotePlugin()`, triggering the plugin's `onEmbedCall` action, which can return values back to the embed.

![Calling the plugin from the embed](https://images.amplenote.com/fae505fa-bd40-11ed-8e3b-9a67e5fef0db/f2ff1507-0b95-436f-9fb1-3ec1d8e6667a.png)

![Embed after clicking the button](https://images.amplenote.com/fae505fa-bd40-11ed-8e3b-9a67e5fef0db/9cd1936e-5d0b-4732-ae88-aa309918ccdf.png)

![Embed after submitting](https://images.amplenote.com/fae505fa-bd40-11ed-8e3b-9a67e5fef0db/3c9861e2-9fdf-4767-8220-1e36da4f2695.png)

### replaceText
Replaces highlighted text via selection menu.

**Arguments:** `app`, `text` (String — selected text)

**Returns:** String (replacement text) or null (cancel replacement)

![replaceText option in the selection menu](https://images.amplenote.com/2ae961e0-bc5d-11ed-808b-e21efa2d8566/06f99dcf-1a52-4093-9f7b-8ab762174e55.png)

![replaceText with a custom keyword](https://images.amplenote.com/fae505fa-bd40-11ed-8e3b-9a67e5fef0db/9f580c1e-57f3-4ec5-b907-ff520f19f8de.png)

### suggestTaskTargetNotes
Suggests ordered notes where tasks could be added.

**Arguments:** `app`, `task`, `suggestedNoteHandles` (Array)

**Returns:** Array of noteHandle objects or UUID strings

![suggestTaskTargetNotes suggested target notes](https://images.amplenote.com/4a2505be-dc5d-11f0-9fc3-f100570d5d30/8b4fe4b0-ae4a-40a0-b99f-0a1a2487298b.png)

### taskOption
Adds options to task commands menu (invoked via `!` in task body).

**Arguments:** `app`, `task`

![taskOption in the task commands menu](https://images.amplenote.com/fae505fa-bd40-11ed-8e3b-9a67e5fef0db/18f9018d-61d0-49fa-82cc-9abe417b377a.png)

### validateSettings
Validates plugin settings when saved, useful for API key verification.

**Arguments:** `app` (limited interface), `settings` (Object)

**Returns:** Array of error strings or falsy value indicating no problems

![validateSettings settings validation example](https://images.amplenote.com/fae505fa-bd40-11ed-8e3b-9a67e5fef0db/eece4bf8-4a9b-4a7d-8982-bc562067fb11.png)
