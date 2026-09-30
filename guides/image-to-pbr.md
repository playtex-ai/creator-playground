# Image to PBR: derive material maps from a surface image

**Image to PBR converts a prepared surface image into channels used by a physically based material.** The PLAYTEX AI PBR Map Generator uses deterministic image processing to derive aligned maps. It does not call an AI model for map derivation, and an image-derived result is not a physical measurement of the photographed material.

[Open PBR Map Generator](https://www.playtex.ai/pbr-map-generator) · [Image-to-PBR website guide](https://www.playtex.ai/image-to-pbr)

## Input and output

Start with a clean, square surface image. If your source is a wider scene, prepare it with the [image-to-texture workflow](image-to-texture.md) first.

The seven map roles are **albedo, normal, roughness, metallic, height, ambient occlusion (AO), and emission**. Not every material needs every map to have nonzero values. For example, ordinary ceramic is not bare metal, and a non-emissive surface should not glow.

## Work through the material

1. Load the approved source into PBR Map Generator.
2. Choose a material intent appropriate to the surface. Check metalness explicitly; brightness alone does not establish that a surface is metal.
3. Inspect the automatically updated preview. Adjust normal and height conservatively so tiny color variations do not become exaggerated relief.
4. Tune roughness while looking at reflections. Roughness describes how spread out the reflection is, not simply whether the source looks dark.
5. Review every map and the repeated material. Keep color maps and data maps distinct.
6. Choose the export resolution and destination supported by your plan. Read the downloaded package's manifest and setup guidance, then test the actual files in the destination.

## A downloadable worked sample

[Download Black & Gold Marble](https://github.com/playtex-ai/creator-playground/releases/download/v1.2.0/playtex-ai-black-gold-marble-512.zip). This actual library material includes six 512px PBR maps, source, Unity packing, and settings. [See its Blender Cycles render and map previews](../assets/materials/black-gold-marble). Existing PLAYTEX AI Terms apply.

For this pack, normal.png is OpenGL (+Y), roughness.png is roughness rather than smoothness, and emission is disabled. Albedo and emission are color/sRGB; normal, roughness, metallic, height, and AO are linear data. Read the [map reference](map-reference.md) before connecting channels.

## Check before shipping

- Test a plane and curved object, then the intended mesh with its real UVs.
- Move the light or environment. Detail should respond naturally rather than appear permanently painted on.
- Inspect tile boundaries, texture scale, and mip/filtering behavior at distance.
- Check normal convention and whether the shader expects roughness or smoothness.
- Match export size to your project's memory budget.

The sample pack is a raw channel set, not an engine-specific package. Generation and file checks do not establish a successful native engine import. See the [public export contract](https://github.com/playtex-ai/playtex-pbr-export-spec) for destination-specific package rules.

Reviewed by PLAYTEX AI, September 30, 2026. [All guides](README.md)
