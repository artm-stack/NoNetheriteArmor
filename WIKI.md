# No Netherite Armor Wiki

## Overview

This mod removes only Netherite armor upgrade outcomes from the smithing table.

Affected vanilla recipe IDs:
- `minecraft:netherite_helmet_smithing`
- `minecraft:netherite_chestplate_smithing`
- `minecraft:netherite_leggings_smithing`
- `minecraft:netherite_boots_smithing`

All other vanilla Netherite upgrades are intentionally left alone.

## How It Works

The mod ships recipe overrides at:
- `src/main/resources/data/minecraft/recipe/netherite_helmet_smithing.json`
- `src/main/resources/data/minecraft/recipe/netherite_chestplate_smithing.json`
- `src/main/resources/data/minecraft/recipe/netherite_leggings_smithing.json`
- `src/main/resources/data/minecraft/recipe/netherite_boots_smithing.json`

Each override keeps the smithing recipe shape but changes the recipe `result` to `minecraft:air`, so no Netherite armor output can be crafted.

## Server Behavior

- Works server-side for gameplay behavior because recipes are datapack-driven.
- Can be installed on both dedicated servers and clients.

## Troubleshooting

If Netherite armor can still be crafted:

1. Confirm the loaded mod jar is `nonetheritearmor-<version>.jar`.
2. Check for another datapack/mod that re-adds or overrides the same four recipe IDs.
3. Verify Fabric Loader and Minecraft versions match this project's `gradle.properties`.

## Updating For New Minecraft Versions

1. Update version properties in `gradle.properties`.
2. Check vanilla JSON structure for the four smithing recipes in the target version.
3. Keep the same four override file names so they replace vanilla recipe IDs.
4. Rebuild and test smithing behavior in-game.
