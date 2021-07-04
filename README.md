# ❗ Important
Whenever you update your settings, go into a creative world and execute `/roguelike settings reload` to check for parsing issues, missing items, or bad references.

These settings are free to be used for personal use, or your modpack or server. 💯 Enjoy.  

## Installation
Insert these settings into your `config/roguelike_dungeons/settings/` directory.

## Directory descriptions
- `base` represents a base, default, no frills, complete dungeon without loot specified. It is intended to be extended into a join-dungeon that also inherits your loot settings.
- `builtin` exposes the builtin dungeons, sans loot, so that you can similarly create a join-dungeon with your custom loot settings.
- `components` is a collection of component-level settings files that can be used to customize a wide variety of dungeons.
- `fnar` is a collection of dungeon settings that I curate from time to time. Feel free to delete them if you do not want these dungeons to spawn.
- `your-namespace` is intended to be renamed, and to serve as your collection of curated dungeon settings. This pack will update from time to time. These updates may require replacing all of the other directories, so keeping your customizations separate enables easy upgrading.

## Adding your own configs
If you add your own configurations, please follow the [namespacing directory structure laid out in the wiki](https://github.com/fnar/minecraft-roguelike/wiki/Dungeon-Settings#directory-structure).
Namespacing your configurations helps to retain your customisations whenever there is a new release of this settings pack.

Build yourself a "main" config that is easily inserted into "dungeon_common.json" for when this pack updates.
See the example at: https://github.com/fnar/minecraft-roguelike-settings/tree/master/settings/fnar/modded/radpack

This "main" config is easily insertable into a 'join'-dungeon that inherits your main and a base dungeon, e.g.:
```json
{
  "name": "your_namespace:dungeon_base",
  "exclusive": false,
  "inherits": [
    "base:dungeon_base",
    "your_namespace:main"
  ]
}
```

This 'join'-dungeon can then be extended (inherited into other dungeons) with more variety and customization, and set to spawn (dungeons set with `exclusive` to `true` will spawn).
