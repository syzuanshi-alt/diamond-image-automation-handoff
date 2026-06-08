# Repeat Report V2

- Set count: 50
- Category counts: {'ring': 30, 'necklace': 10, 'earrings': 5, 'bracelet': 5}
- Lens group counts: {'normal': 38, 'mild': 9, 'special': 3}
- Unique combination keys: 50
- Duplicate combination keys: 0
- Window repeat issues: 4

## Notes

- No duplicate full combination keys found.
- Some recent-window repeat issues found; inspect JSON.

## V2 Fixes

- Macro prompt now includes full Product DNA instead of only saying Same Product DNA.
- Full-body prompt now prioritizes outfit/body/environment and avoids detail-only contradiction.
- Persona, scene, and outfit are selected from compatible clusters.

## Lens Target

- Expected for 50: normal 35-40, mild 8-10, special 3-5.
- Actual: {'normal': 38, 'mild': 9, 'special': 3}