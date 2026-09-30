# PBR material and skybox handoff for Blender, Unity, Unreal, Godot, Three.js, and Roblox

**A texture pack becomes a material only when its channels are connected correctly in the destination.** These sample packs contain raw PNG maps and descriptive metadata. They do not include native engine projects, importers, executable helpers, or prepacked engine textures.

## Blender starting point

Use a mesh with UVs and a Principled BSDF material. Connect albedo as color to Base Color. Load roughness and metallic as Non-Color data and connect them to their corresponding inputs. Load normal as Non-Color and pass it through a tangent-space Normal Map node before the shader's Normal input. Keep height/displacement disabled initially; establish scale and a sane normal response first. The sample emission map is black.

See the [Blender Normal Map node documentation](https://docs.blender.org/manual/en/latest/render/shader_nodes/displacement/normal_map.html) for the node's data and coordinate-space requirements. This release's files were checked locally; it is not a claim of a tested .blend delivery.

## Destination decisions

| Destination | Check before importing |
| --- | --- |
| Unity URP | Shader-specific metallic/smoothness packing; do not treat the standalone roughness image as a ready-made packed map. |
| Unity HDRP | Mask-map channel packing and the chosen material shader. |
| Unreal Engine | DirectX normal convention and data-map import settings; these samples begin as OpenGL normals. |
| Godot | UV scale, normal convention, and material texture multipliers. |
| Three.js | Color management and shader channel expectations; the skybox face order is px, nx, py, ny, pz, nz. |
| Roblox | Use the dedicated SurfaceAppearance/skybox workflow and confirm its image assignments and rotations. |

PLAYTEX AI's actual PBR Map Generator engine packages provide destination-specific guidance. The [public package matrix](https://github.com/playtex-ai/playtex-pbr-export-spec/blob/main/docs/engine-package-matrix.md) describes those exports; the [verification boundary](https://github.com/playtex-ai/playtex-pbr-export-spec/blob/main/docs/verification-boundary.md) explains what has and has not been tested.

## Useful product walkthroughs

- [Import PBR textures into Roblox Studio](https://www.playtex.ai/blog/importing-playtex-textures-into-roblox)
- [PBR Map Generator](https://www.playtex.ai/pbr-map-generator)
- [Skybox generation and projection](skybox-generator.md)
- [Map meanings and troubleshooting](map-reference.md)

Reviewed by PLAYTEX AI, September 30, 2026. [All guides](README.md)
