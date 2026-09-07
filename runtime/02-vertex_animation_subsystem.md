---
order: -2
---

# Vertex Animation Subsystem

This is a subsystem that makes it easy to create and update instances without worrying about the technology under the hood. <br/>
It provides functions for handling instances which are exposed to blueprint.

!!! warning
The material of the static mesh must have **Used with Instanced Static Meshes** enabled, otherwise the instances render with the default material. Enable it in the material Details panel under **Usage** and save the material.
!!!

## Functions

```cpp
//When this function is called, the subsystem will create an ISM for the mesh if needed. It will also apply the given world transform.
int AddInstance(UStaticMesh* StaticMesh, const FTransform& Transform);
```

```cpp
TArray<int> AddInstances(UStaticMesh* StaticMesh, const TArray<FTransform>& Transforms);
```

```cpp
TArray<FVertexAnimationInstanceInfo> GetInstances(UStaticMesh* StaticMesh) const;
```

```cpp
bool RemoveInstanceByIndex(UStaticMesh* StaticMesh, int Index);
```

```cpp
bool RemoveInstanceById(UStaticMesh* StaticMesh, int Id);
```

```cpp
bool RemoveInstancesByIndex(UStaticMesh* StaticMesh, const TArray<int>& Indices);
```

```cpp
bool RemoveInstancesById(UStaticMesh* StaticMesh, const TArray<int>& Ids);
```

```cpp
bool UpdateInstanceTransformById(UStaticMesh* StaticMesh, int Id, const FTransform& Transform);
```

```cpp
bool UpdateInstanceTransformByIndex(UStaticMesh* StaticMesh, int Index, const FTransform& Transform);
```

```cpp
bool BatchUpdateInstancesTransform(UStaticMesh* StaticMesh, int StartIndex, int Num, const FTransform& Transform);
```

```cpp
bool BatchUpdateInstancesTransforms(UStaticMesh* StaticMesh, int StartIndex, const TArray&lt;FTransform&gt;&amp; Transforms);
```

```cpp
bool SetCustomDataById(UStaticMesh* StaticMesh, int Id, int CustomDataIndex, float Value);
```

```cpp
bool SetCustomDataByIndex(UStaticMesh* StaticMesh, int Index, int CustomDataIndex, float Value);
```

```cpp
int GetIndexFromId(UStaticMesh* StaticMesh, int Id) const;
```

```cpp
int GetIdFromIndex(UStaticMesh* StaticMesh, int Index) const;
```
