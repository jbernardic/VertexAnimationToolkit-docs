# Max Texture Size

**Max Texture Size** is the upper limit for the dimensions of the position and normal
texture arrays that **Bake VAT** generates. The toolkit never creates a texture larger
than this value on either axis.

## Where to change it

1. Open **Edit → Project Settings**.
2. Under the **Plugins** category, select **VertexAnimationToolkit**.
3. Set **Max Texture Size** from the dropdown.

::: tip
The setting is saved per project (Editor Per-Project User Settings) and is applied the
next time you bake. There is no longer a popup during baking &mdash; the value always
comes from here.
:::

## What it does

Each baked vertex maps to one texture column, and each animation frame maps to one row.
When a mesh has more vertices or more frames than the **Max Texture Size**, the data is
split across multiple slices of a texture array.

Within that limit, the toolkit automatically picks the **smallest size that still fits your
mesh and animation**, so textures are not padded with empty space. The vertex (width) and
frame (height) axes are sized independently.

- **Lower** values keep individual textures small, but very large meshes or long
  animations will be split into more texture-array slices.
- **Higher** values allow everything to fit in fewer slices, at the cost of a higher
  potential maximum texture size.

::: tip
For most assets the default of **8192** is the best choice: it lets the toolkit fit
the texture tightly while keeping the slice count to a minimum. Only lower it if you need
to cap texture dimensions for a specific platform or memory budget.
:::

## Available sizes

`8192`, `4096`, `2048`, `1024`, `512`, `256`, `128`, `64`, `32`, `16`, `8` (powers of two).
