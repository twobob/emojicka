# Emojicka

A tiny browser-based world rendered on a canvas with procedurally generated biomes, gold to collect, shoals of fish using lightweight flocking, land animals with centralised behaviour (cheap wandering + occasional pathing), and NPCs drawn as emojis with overlaid animated legs.

## Features

- Procedural world: deep/shallow water, beaches, grassland, forest, desert, and rock.
- Player movement: click-to-move with boat embark/disembark handled automatically.
- Gold rush: gold spawns on land; collecting shows a brief floating emoji.
- Fish: very cheap flocking with staggered updates, local neighbour lookups, and off-screen culling.
- Land animals: centralised behaviour with smooth speed changes, low-cost wandering, and limited-budget pathfinding.
- NPCs: emoji characters rendered with simple animated “stick legs”.
- Minimap: shows nearby terrain, boats, and gold.

## How to run

- Open `Emojicka.html` directly in a modern desktop browser.
- Resize the window as you like; the canvas adapts.

## Controls

- Click anywhere on the map to set a destination.
- The player will board a nearby boat when needed and disembark at a beach.

## Performance notes

- Fish updates are view-aware and use a micro spatial hash; only on-screen or near the player are updated.
- Land animal pathfinding is budgeted per frame and constrained to a local search radius.
- Shared helpers reduce duplication and keep behaviours consistent.

## Troubleshooting

- If performance dips, reduce spawn caps or increase update intervals.
- Different platforms render emojis differently; NPC appearance may vary by font.

## Licence

MIT