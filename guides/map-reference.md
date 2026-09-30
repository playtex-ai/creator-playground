# PBR texture map reference and troubleshooting

The sample pack contains separate maps. Connect each one according to its meaning; a filename alone is not an instruction to enable every shader input.

| File | Meaning | Sample color treatment | First check |
| --- | --- | --- | --- |
| albedo.png | Base surface color | sRGB / color | Avoid interpreting baked highlights as real reflectance. |
| normal.png | Tangent-space surface direction | Linear data | Samples use OpenGL (+Y). |
| roughness.png | Reflection spread | Linear data | White is rougher; this file is not smoothness. |
| metallic.png | Metallic material response | Linear data | Classify the material, not just source brightness. |
| height.png | Relative relief | Linear data | Not calibrated distance; choose shader scale carefully. |
| ao.png | Local occlusion estimate | Linear data | Not a replacement for scene lighting or all shadows. |
| emission.png | Emissive color | sRGB / color | Samples disable emission and include a black map. |

## Troubleshooting

| Result | Likely check |
| --- | --- |
| Grooves look raised | Confirm the normal convention and avoid flipping green twice. |
| Material looks too shiny | Check roughness versus smoothness and shader multipliers. |
| Wood or ceramic looks metallic | Review the metallic map and material class. |
| Surface looks inflated | Reduce normal/height strength and review UV scale. |
| Texture is stretched | Check mesh UVs and aspect ratio. |
| Gray data maps look wrong | Ensure the importer is treating them as data, not sRGB color. |
| Sky looks correct but lighting is weak | A background image and an HDR illumination source serve different purposes. |

For actual PLAYTEX AI engine-package naming, packing, and manifest fields, use the [export specification](https://github.com/playtex-ai/playtex-pbr-export-spec). The sample metadata here describes raw files and does not impersonate an engine export manifest.

Reviewed by PLAYTEX AI, September 30, 2026. [All guides](README.md)
