# No Netherite Armor (Fabric)

`No Netherite Armor` is a Fabric mod that disables Netherite armor crafting only.

## What This Mod Does

- Blocks `diamond_helmet -> netherite_helmet`.
- Blocks `diamond_chestplate -> netherite_chestplate`.
- Blocks `diamond_leggings -> netherite_leggings`.
- Blocks `diamond_boots -> netherite_boots`.
- Leaves all non-armor Netherite recipes unchanged (for example, Netherite tools).

Implementation detail:
- The mod overrides only the four vanilla armor smithing recipe files under `data/minecraft/recipe/`.
- Runtime code is minimal; behavior is data-driven.

## Compatibility

- Minecraft: `26.1.1`
- Fabric Loader: `>=0.18.4`
- Java: `>=25`

## Install

1. Build or download the jar.
2. Place `build/libs/nonetheritearmor-<version>.jar` in your Fabric `mods` folder.
3. Start the game/server with Fabric Loader.

## Build

```powershell
.\gradlew build
```

Artifacts are written to `build/libs/`.

## GitHub Release / Deployment

1. Bump `mod_version` in `gradle.properties`.
2. Run `.\gradlew build`.
3. Create a Git tag (example: `v1.0.1`).
4. Create a GitHub Release for that tag.
5. Upload `nonetheritearmor-<version>.jar` from `build/libs/`.

## Notes

- A legacy datapack example is included in this repository as `Remove Netherite Armor.zip`.
- This mod version applies the same core idea in a Fabric mod project structure.
