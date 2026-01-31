\page baseuse Quick Use

# Use pre-created actor with component
- Spawn actor class in level: **ASplineMeshed** class
- Create child actor class from: **ASplineMeshed** class

# Add component to your actor in BP
Use one of this:
- Attach component to actor in component tree
- Spawn during runtime: Search for "Spawn From Class"
 - Promote object to variable to keep it alive
 - This is only required to keep object alive during gameplay and prevent UE from destroying it.

---

# Use in C++

To access Spline Meshed component or class:
```cpp
#include "SplineMeshedComponent.h" /// Just component
#include "SplineMeshedActor.h"  /// Precreated actor with attached component and functions
```

It is **UObject**, so it must comply with unreal engine rules for objects lifecycle.
Store ref value as any UObject if you want it to persist in game for longer.
```cpp
/* Declaration in class, write initialization in CDO */
UPROPERTY()
TObjectPtr<USplineMeshedComponent> SplineMeshCmp;
```
## Classes hierarchy 
Core component:
- \ref USplineMeshedComponent : core component
- \ref USplineMeshedComponent_Extension : modified component

Classes:
- \ref ASplineMeshed : Actor with core component
- \ref ASplineMeshed_AbstractExtension : Actor with modified component

---

# Extending functionality
Class has exposed function to use and override modification of every mesh for custom desire.
- Create child class of any component:
  - Override function [OnMeshSpawn](@ref USplineMeshedComponent::OnMeshSpawn) (for spawn customization)
  - Override function [Detection](@ref USplineMeshedComponent::DetectionFunction) (for collision detection)

