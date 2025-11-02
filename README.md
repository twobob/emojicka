# Emojicka

A browser-based procedural world game with emoji-based graphics, featuring infinite terrain generation, pathfinding, NPC settlements, and multiple movement modes.

## Features

- **Procedural world generation**: Infinite chunk-based terrain with biomes including water (deep/shallow), beaches, grassland, forest, desert, impassable rocks, climbable mountains, and snow
- **Settlements**: Cities, towns, and villages with unique NPCs (royalty, commoners, undead)
- **Player movement**: 
  - Click-to-move with A* pathfinding
  - Automatic boat usage and swimming
  - Mountain climbing and snow traversal (skiing/snowboarding)
  - Diagonal movement with obstacle detection
  - Direction-aware emoji display
- **Navigation**: 
  - World map (W key) - view entire explored world, click to travel
  - Minimap - shows nearby terrain, boats, and gold
  - Debug mode (D key) - visual position indicators
- **NPCs**: Settlement-based characters with dialogue and unique roles (King, Queen, zombies, vampires)
- **Gold collection**: Randomly spawned collectibles with visual feedback
- **Wildlife**: Flocking fish in deep water, wandering land animals with AI pathfinding
- **Safe spawn**: Player always starts on walkable terrain

## Controls

- **Left Click**: Set destination (main canvas, minimap, or world map)
- **W**: Toggle world map overlay
- **D**: Toggle debug mode
- Movement modes (boat, swimming, climbing, skiing) activate automatically based on terrain

## Technical Details

- **Chunk-based generation**: On-demand 40×40 tile chunks using Perlin noise
- **Pathfinding**: A* algorithm with terrain-aware cost calculations
- **Terrain types**: 12 distinct tiles with different movement properties
- **Movement speeds**: Configurable base speed (300 px/s) with terrain modifiers (swimming 5x slower, climbing 25x slower, etc.)
- **Performance**: View-culled fish rendering, budget-limited animal pathfinding, spatial hashing

## Installation

Open `index.html` in a modern browser. No build process or dependencies required.

## Notes

- Emoji appearance varies by platform/font
- World map displays explored chunks; unexplored areas shown as black
- Click on impassable rocks navigates to nearest walkable tile

## Licence

MIT
