# Material to PBR: give an existing surface a usable material response

**Material to PBR usually means taking an existing material image—such as a wood texture, stone surface, or metal pattern—and preparing the channels a PBR shader needs.** In PLAYTEX AI, use PBR Map Generator for this task. If you already have measured maps, preserve their known meanings instead of assuming an image-derived replacement will be more accurate.

[Open PBR Map Generator](https://www.playtex.ai/pbr-map-generator)

## Decide what your input actually is

| Starting point | Best next step |
| --- | --- |
| A photo of a room containing a surface | Isolate a texture with [image to texture](image-to-texture.md). |
| One prepared surface image | Derive maps using [image to PBR](image-to-pbr.md). |
| An existing complete PBR set | Inspect channel meanings, normal convention, scale, and destination packing before regenerating anything. |
| A native material from another engine | Identify its textures and shader behavior; a native material graph is not interchangeable with one image. |

## Three materials, three decisions

**Mint Terrazzo:** treat it as a dielectric surface. Tune relief so the colored chips do not automatically look like deep holes. [Sample](../assets/materials/mint-terrazzo).

**Peach Ceramic:** inspect the tile joints and glossy response separately. Smoothness is not the same as a bright base color. [Sample](../assets/materials/peach-ceramic).

**Midnight Metal:** the pack uses a bare-metal intent. Reflections need something to reflect, so judge it under useful environment lighting. A painted metal object may need a coated-material interpretation instead. [Sample](../assets/materials/midnight-metal).

These are stylized demonstration sources, not measured material references. Their settings are starting points, not universal presets for real terrazzo, ceramic, or metal.

## Finish the material

1. Choose a material class and inspect the resulting channels.
2. Set a believable repeat scale on the intended mesh.
3. Compare roughness and normal detail under more than one light direction.
4. Decide whether height is needed by your shader. A height texture does not change collision geometry by itself.
5. Export and inspect the actual files, then follow the [engine handoff guide](engine-handoff.md).

## Common mistake: reading photographed light as geometry

A dark patch can be a shadow, dirt, paint, or a depression. A bright patch can be a highlight rather than a metal surface. Deterministic processing can derive useful channels from image information, but the image alone does not establish the true physical cause. Clean the source and make material decisions deliberately.

Reviewed by PLAYTEX AI, September 30, 2026. [All guides](README.md)
