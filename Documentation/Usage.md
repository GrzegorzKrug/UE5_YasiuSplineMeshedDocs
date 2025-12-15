\page baseuse Quick Use

# Use pre-created actor class
- Spawn actor class in level: **ASplineMeshed** class
- Create child actor class from: **ASplineMeshed** class

# Use component in Blueprints
Use one of this:
- Attach component to actor in component tree
- Spawn during runtime: Search for "Spawn From Class"
 - Promote object to variable to keep it alive
 - This is only required to keep object alive during gameplay and prevent UE from destroying it.

---

# Use in C++

To access Spline Meshed component or class:
```cpp
#include "SplineMeshedComponent.h"
#include "SplineMeshedActor.h"
```

It is **UObject**, so it must comply with unreal engine rules for objects lifecycle.
Store ref value as any UObject if you want it to persist in game for longer.
```cpp
/* Declaration in class, initialize in CDO */
UPROPERTY()
TObjectPtr<USplineMeshedComponent> SplineMeshCmp;
```
## Classes hierarchy 
Core component:
- \ref USplineMeshedComponent : core component
- \ref USplineMeshedComponent_ExtensionBridge : modified component

Classes:
- \ref ASplineMeshed : Actor with core component
- \ref ASplineMeshed_AbstractExtension : Actor with modified component

---

# Extending functionality
Class has exposed function to use and override modification of every mesh for custom desire.
- Create child class of any component and overwrite function [Extend](@ref USplineMeshedComponent::Extend)

