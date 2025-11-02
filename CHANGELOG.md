# Changelog

## Recent Updates

### Navigation & Controls
- Fixed world map click coordinate conversion (canvas scaling)
- Fixed minimap click coordinate conversion (canvas scaling)
- Removed blocking check that prevented swimming to water

### Terrain & Graphics
- Restored rock placement on grass tiles using noise (natural obstacles)
- Changed mountain rocks from emoji to light grey overlay (#D3D3D3)
- Fixed gold spawning to avoid placement on impassable rocks

### Player Movement
- Fixed player direction updating during automove
- Fixed emoji flickering when standing still on special terrain
- Clear movement states (swimming, climbing, skiing) when path completes
- Swimming emoji now flips correctly in all directions

### World Generation
- Boats now spawn in shallow water/beaches adjacent to islands
- Each coastal chunk gets a boat ensuring island accessibility
- Fixed climbing emoji syntax error

### Code Cleanup
- Removed obsolete commented code blocks
- Cleaned up defensive NaN validation checks after fixing root cause
