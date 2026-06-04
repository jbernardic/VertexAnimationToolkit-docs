# Runtime

To use vertex animation textures in your game, you can use one of the following systems:

=== ISM or HISM
Use this if you need fine-grained control over how your instances are rendered. You should also be willing to configure it yourself for optimization.
<br>[About ISM or HISM](../runtime/01-ism_hism.md)
===

=== Vertex Animation Subsystem
Abstracts ISM and HISM in a properly optimized way.
Provides Blueprint functions to render instances.
It is easy to use, but lacks some of the flexibility that using ISM / HISM itself provides.
<br>[About Vertex Animation Subsystem](../runtime/02-vertex_animation_subsystem.md)
===

=== Vertex Animation Instance Component
Renders instances on top of your actors. Useful for individual actor logic, but lacks performance due to actor overhead.
<br>[About Vertex Animation Instance](../runtime/03-vertex_animation_instance.md)
===
