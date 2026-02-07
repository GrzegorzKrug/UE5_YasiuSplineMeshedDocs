\page issues Known Issues


#### Buttons
@note Some buttons should not be visible in editor and caused crash.
- Buttons are still visible in Blueprint editor window 
- Functions are disabled and no message is displayed.

---

#### Undo (Ctrl+Z)
@note Using undo/redo was causing problem by not tracking meshes correctly.
- It is safe to use
- On `Undo` Meshes will be destroyed and new will be created in new construction pass. (only internal meshes stored in component)

---
