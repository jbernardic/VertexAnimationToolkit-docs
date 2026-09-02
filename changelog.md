

# Changelog

=== <b>Update 1.2.9</b> _9/2/2026_
- Fixed broken playback when an animation has more frames than <b>Max Texture Size</b> (frame tiling now samples the correct texture slice and row)
- Fixed baking when <b>both</b> the vertex count and the frame count exceed <b>Max Texture Size</b> (re-bake affected assets after updating)
- Removed the <b>Texture Size</b> input from the Play Animation node — texture dimensions are now read from the texture automatically
===

=== <b>Update 1.2.8</b> _6/4/2026_
- Reduced generated texture memory by up to <b>~55%</b> by sizing the position/normal texture arrays to fit the mesh and animation instead of always padding to the maximum size
- Vertex (width) and frame (height) axes are now sized independently to avoid wasted texture space
- Texture size is now set in <b>Project Settings</b> as <b>Max Texture Size</b> (no more bake-time popup)
- Minor bugs fixed
===

=== <b>Update 1.2.3</b> _5/17/2025_
- Bypass previous vertex and frame count limitations
- Minor bugs fixed
===

=== <b>Update 1.2.0</b> _1/25/2025_
- Added support for multiple <b>LODs</b> 
- Added automatic vector calculation 
- Added <b>Vertex Animation Subsystem</b> 
- Added <b>Play Once</b> in Play Animation node
===

=== <b>Update 1.1.1</b> _10/31/2024_
- Added support for <b>UE 5.5</b>
===

=== <b>Update 1.1.0</b> _9/26/2024_
- Easy Instanced Static Mesh setup 
- Minor bugs fixed 
- Support for <b>UE 5.2 - 5.4</b>
===