# Installing & Using Amplenote Plugins

> [← Help Index](../00-index.md) · Category: [Extending Amplenote](./index.md) · [Source ↗](https://www.amplenote.com/help/installing_and_using_plugins)

## Installation Methods

Amplenote provides three ways to install plugins:

1. Use the install button in the [Published Plugins Directory](https://www.amplenote.com/help/published_plugins_directory)
2. Substitute a note token into this URL: `https://www.amplenote.com/account/plugins?source-token=[TOKEN]`
3. Visit Account Settings → Plugins and enable a note you created or received as a plugin

![This view of the plugins page will be outdated by April or May 2023, but still including it cuz a section without a screenshot is the pits](https://images.amplenote.com/47377476-ceb0-11ed-898c-76979436bcb1/4362ca46-ee21-4e8c-9c2c-a915b4fc6ec3.png)

## Plugin Management

"Plugins are managed by opening Account Settings, choosing the plugins tab, and clicking to enable the note as a plugin whose commands will become available."

## Updating Plugins

To update plugins, navigate to Settings → Plugins and look for a refresh icon. Click it, then confirm the update prompt. Note that "settings you chose for your plugin will be preserved, unless the author changed the name of the settings (rare)."

![Click the yellow refresh icon to initiate an update](https://images.amplenote.com/47377476-ceb0-11ed-898c-76979436bcb1/c0e40cba-c217-44e5-83e0-dc63e3368af4.png)

![Confirming the plugin update prompt](https://images.amplenote.com/47377476-ceb0-11ed-898c-76979436bcb1/36deaf06-07e9-4e8a-a1b7-bd4a119396f3.png)

## Security Considerations

Plugins can access note content and make calls to external websites, but only when invoked. The code is "completely isolated from the app. It can't get anything not provided to it, though note content is provided to it."

## Performance Impact

Plugins cannot run on every keystroke. Their effects are "generally limited to when you interact with them (via context menu, note menu, etc)."

## Plugin Development

Building plugins requires only JavaScript knowledge—"no need to download an IDE or speak git." The [plugin development guide](https://www.amplenote.com/help/developing_amplenote_plugins) provides complete specifications.
