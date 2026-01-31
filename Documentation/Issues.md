\page issues Known Issues

### Temporary objects
@warning Using undo/redo can create visual artifacts of spawned mesh objects
- Due to optimization meshes are not flagged for auto clean and are persistent.
- It can cause temporary object hanging as part of actor/component.
- Meshes will not be saved and will disappear after restart (or level change).

---
