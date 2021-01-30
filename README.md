# ❗ Important
Whenever you update your settings, go into a creative world and execute `/roguelike settings reload` to check for parsing issues, missing items, or bad references.

These settings are free to be used for personal use, or your modpack or server. 💯 Enjoy.  

## Installation
Insert these settings into your `config/roguelike_dungeons/settings/` directory.

## Updating  
When new settings are released, you will only have to:
- download the new settings from the release page
- delete the `fnar/` namespace (directory)
- unpack the new settings (with the latest `fnar/` namespace)
- insert your main config's name (e.g. `"main:rad"` is in the name field of `main_rad.json`) into the list of inherited settings of `dungeon_common.json`
- 🎉

## Adding your own configs
If you add your own configurations, please follow the [namespacing directory structure laid out in the wiki](https://github.com/fnar/minecraft-roguelike/wiki/Dungeon-Settings#directory-structure).
Namespacing your configurations helps to retain your customisations whenever there is a new release of this settings pack.

Build yourself a "main" config that is easily inserted into "dungeon_common.json" for when this pack updates.
See the example at: https://github.com/fnar/minecraft-roguelike-settings/tree/master/settings/fnar/modded/radpack