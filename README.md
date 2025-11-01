# Emojicka

A tiny browser-based world rendered on a canvas with procedurally generated biomes, settlements, NPCs, gold to collect, shoals of fish using lightweight flocking, land animals with centralised behaviour, and a player character with smooth movement and multiple traversal modes.

## Features

- **Procedural world generation**: Deep/shallow water, beaches, grassland, forest, desert, rocks, and snow-capped mountains using 3D Perlin noise for terrain height.
- **Settlements**: Procedurally placed cities, towns, and villages with unique NPCs including royalty and an undead village.
- **Player movement**: 
  - Smooth lerp-based movement with configurable speed
  - Click-to-move with A* pathfinding
  - Automatic boat embark/disembark
  - Swimming ability (4x slower than walking, used as fallback when no boat available)
  - Diagonal movement with corner-cutting prevention
- **World map**: Press `W` to view entire explored world, click to set destinations
- **Minimap**: Shows nearby terrain, boats, and gold (click to navigate)
- **Debug mode**: Press `D` to toggle visual debugging showing player position, tile centers, and boundaries
- **NPCs**: 
  - Categorized into royal, common, and undead types
  - Unique King and Queen
  - Undead village with zombies and vampires
  - Speech bubbles with character-specific dialogue
- **Gold collection**: Gold nuggets spawn on land with floating emoji feedback on collection
- **Fish**: Efficient flocking with staggered updates, local neighbour lookups, and off-screen culling
- **Land animals**: Centralized behaviour with smooth speed changes, low-cost wandering, and budget-limited pathfinding
- **Safe spawn**: Player spawns in walkable areas using concentric circle search

## How to run

- Open `index.html` directly in a modern desktop browser
- No build process or dependencies required
- Resize the window as needed; canvas adapts automatically

## Controls

- **Left Click**: Set destination (works on main map, minimap, and world map)
- **W**: Toggle world map overlay (pauses game)
- **D**: Toggle debug mode (shows position indicators)
- Player automatically boards boats when needed and disembarks at beaches
- Swimming is automatic when crossing water without a boat

## Technical highlights

- **Chunk-based world generation**: Infinite procedural world with on-demand chunk generation
- **A* pathfinding**: With diagonal movement, boat transitions, and swimming support
- **Performance optimizations**:
  - Fish updates are view-aware with micro spatial hash
  - Animal pathfinding is budgeted per frame with local search radius
  - Shared helper functions for consistency
- **Movement constants** (easily configurable):
  - `PLAYER_SPEED`: 300 pixels/second
  - `SWIMMING_SPEED_MULTIPLIER`: 0.25 (4x slower)
  - `SWIMMING_PATHFINDING_COST`: Auto-calculated from speed multiplier

## Performance notes

- Fish updates target only on-screen or near-player entities
- Land animal pathfinding is budget-limited per frame
- Chunk generation happens on-demand as player explores
- Reduce spawn caps or increase update intervals if performance dips

## Troubleshooting

- Different platforms render emojis differently; appearance may vary by font
- World map shows all explored chunks; unexplored areas appear black
- If player gets stuck, swimming can be used to escape (slower but always available)

## Licence

MIT
