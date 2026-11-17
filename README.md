# Frost Mage

A mod for [Azeroth Survivors Reborn](https://azreborn.com), and the first package of its community catalog
([Syiana/azs-mods](https://github.com/Syiana/azs-mods)). It gives the mage a frost starter and changes nothing else.

| | Stock mage | With this mod |
| --- | --- | --- |
| Starter | Fireball, a single-target fire bolt | **Glacial Pulse**, a frost nova (radius 8, hit 18, every 2 s, range 8) |
| Rider | none | roots what it hits for 2 s |
| Resource | none | **Chill** (up to 3), built by every pulse |
| Health | stock | 260 |

It is data only: `packs/syiana.frostmage/pack.toml` names the pack, `archetype.toml` overrides `class:mage` and
`spell:fireball`. Every name carries all twelve languages.

## Installing it

In the game, open the MODS tab (AddOns window; MENU > Mods in versions that have it), go to **Community packages**
and press **Install**. It plays as **Modded**, with saves and progress of its own; the official game is untouched.

## Building the release zip

A package version is a locked profile: `profile.json`, `LICENSE` and exactly the files the lock names (the mod's
own pack and the official packs it depends on). With the game's maintainer tools:

```bash
azs-release profile-lock <profile folder>
azs-release profile-pack <profile folder> --out frostmage-v1.zip
```

`profile-lock` hashes every locked file again and runs the game's own source check; `profile-pack` writes the same
bytes every time and prints the size and SHA-256 that the registry pins.

## License

The files under `packs/syiana.frostmage/` are MIT (see `LICENSE`). The official packs inside a release zip are the
game's own content and are not covered by it.
