# Installing & Using Amplenote Plugins

> [← Help Index](../00-index.md) · Category: [Extending Amplenote](./index.md) · [Source ↗](https://www.amplenote.com/help/installing_and_using_plugins)

## Installation Methods

Amplenote provides four ways to install plugins:

1. Use the install button in the [Published Plugins Directory](https://www.amplenote.com/help/published_plugins_directory)
2. Substitute a note token into this URL: `https://www.amplenote.com/account/plugins?source-token=[TOKEN]` (for example, `ShS4jpYLAAHGWqrDmFt4jXyb` installs via `https://www.amplenote.com/account/plugins?source-token=ShS4jpYLAAHGWqrDmFt4jXyb`)
3. Visit Account Settings → Plugins and enable a note you created or received as a plugin
4. From the plugin note itself (easiest): open the plugin note, click the note options menu ("…" top-right), then choose "Install plugin" at the bottom of the menu

![The plugin note options menu with Install plugin](https://images.amplenote.com/47377476-ceb0-11ed-898c-76979436bcb1/dbc787b2-898a-46be-8fea-05d2a79cbfe3.png)

![The plugin note options menu](https://images.amplenote.com/47377476-ceb0-11ed-898c-76979436bcb1/2f56ffdc-c276-452a-96dd-5550303cc5eb.png)

![This view of the plugins page will be outdated by April or May 2023, but still including it cuz a section without a screenshot is the pits](https://images.amplenote.com/47377476-ceb0-11ed-898c-76979436bcb1/4362ca46-ee21-4e8c-9c2c-a915b4fc6ec3.png)

## Plugin Management

"Plugins are managed by opening Account Settings, choosing the plugins tab, and clicking to enable the note as a plugin whose commands will become available."

## Updating Plugins

To update plugins, navigate to Settings → Plugins and look for a refresh icon. Click it, then confirm the update prompt. Note that "settings you chose for your plugin will be preserved, unless the author changed the name of the settings (rare)." If you changed the code of the plugin after installing it, you will need to re-apply those changes after you update.

![Click the yellow refresh icon to initiate an update](https://images.amplenote.com/47377476-ceb0-11ed-898c-76979436bcb1/c0e40cba-c217-44e5-83e0-dc63e3368af4.png)

![Confirming the plugin update prompt](https://images.amplenote.com/47377476-ceb0-11ed-898c-76979436bcb1/36deaf06-07e9-4e8a-a1b7-bd4a119396f3.png)

## Security Considerations

A plugin can access vault notes (assuming they have been unlocked by a password), can call whatever website it wants, and can (to some degree now, and definitely in the future) execute code even when not invoked directly. The code is visible, but could be obfuscated pretty easily. The plugin is isolated from the app: it can't touch cookies or call Amplenote servers with any privileges, though note content is provided to it.

## Performance Impact

Plugins cannot run on every keystroke. Their effects are generally limited to when you interact with them (via context menu, note menu, etc). However, plugins can potentially set up timers that allow them to be executed after their time of invocation. A careless or malevolent author could also create huge volumes of notes, or generate notes with more content than can fit into memory.

## Plugin Development

Building plugins requires only JavaScript knowledge—"no need to download an IDE or speak git." The [plugin development guide](https://www.amplenote.com/help/developing_amplenote_plugins) provides complete specifications.
