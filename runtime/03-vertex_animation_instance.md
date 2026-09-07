---
order: -3
---

# Vertex Animation Instance (component)

Use this if you want to use vertex animations for individual actors in the scene.
For each actor that contains the component, this component will create and update ISM / HISM instances automatically.

To use it, simply add this component to your actor and set its **Static Mesh**. Instance of it will be created based on actors transform.

!!! warning
The material of the static mesh must have **Used with Instanced Static Meshes** enabled, otherwise the instances render with the default material. Enable it in the material Details panel under **Usage** and save the material.
!!!

## Properties
![](../assets/VertexAnimationInstance_1.png)

## Functions
![](../assets/VertexAnimationinstance_2.png)
