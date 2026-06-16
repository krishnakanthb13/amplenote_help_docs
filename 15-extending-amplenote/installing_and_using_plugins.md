# Installing & Using Amplenote Plugins

> [← Help Index](../00-index.md) · Category: [Extending Amplenote](./index.md) · [Source ↗](https://www.amplenote.com/help/installing_and_using_plugins)

## Installation Methods

Amplenote provides three ways to install plugins:

1. Use the install button in the [Published Plugins Directory](https://www.amplenote.com/help/published_plugins_directory)
2. Substitute a note token into this URL: `https://www.amplenote.com/account/plugins?source-token=[TOKEN]`
3. Visit Account Settings → Plugins and enable a note you created or received as a plugin

## Plugin Management

"Plugins are managed by opening Account Settings, choosing the plugins tab, and clicking to enable the note as a plugin whose commands will become available."

## Updating Plugins

To update plugins, navigate to Settings → Plugins and look for a refresh icon. Click it, then confirm the update prompt. Note that "settings you chose for your plugin will be preserved, unless the author changed the name of the settings (rare)."

## Security Considerations

Plugins can access note content and make calls to external websites, but only when invoked. The code is "completely isolated from the app. It can't get anything not provided to it, though note content is provided to it."

## Performance Impact

Plugins cannot run on every keystroke. Their effects are "generally limited to when you interact with them (via context menu, note menu, etc)."

## Plugin Development

Building plugins requires only JavaScript knowledge—"no need to download an IDE or speak git." The [plugin development guide](https://www.amplenote.com/help/developing_amplenote_plugins) provides complete specifications.
