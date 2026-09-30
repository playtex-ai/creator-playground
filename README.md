<p align="center"><a href="https://www.playtex.ai/?utm_source=github&utm_medium=referral&utm_campaign=creator_playground"><img src="media/showcase/playtex-ai-creator-playground.png" alt="PLAYTEX AI Creator Playground: image to texture, image to PBR, and skybox workflows with the official rabbit logo and real product artwork" width="100%"></a></p>

# PLAYTEX AI — Image to Texture, Image to PBR & Skybox Generator Guides

**Your next world starts with a surface.** This is the PLAYTEX AI Creator Playground: practical workflows, real product examples, a free photo-derived PBR sample, and creative challenges for game developers and 3D artists.

[**Try PLAYTEX AI ↗**](https://www.playtex.ai/?utm_source=github&utm_medium=referral&utm_campaign=creator_playground) · [**Download the real wood PBR pack ↓**](https://github.com/playtex-ai/creator-playground/releases/download/v1.1.0/playtex-ai-wood-photo-pbr-512.zip) · [**Choose a guide →**](guides/README.md)

PLAYTEX AI offers browser-based image-to-texture, image-to-PBR, material, and skybox workflows. AI-assisted tools create source imagery; the **PBR Map Generator uses deterministic image processing** to derive material maps. This public repository contains documentation and assets. The tools run on the website and their implementation stays private.

## 🧭 What are you making?

| Start with… | Make… | Follow the workflow | Open the tool |
| --- | --- | --- | --- |
| A photo, screenshot, or artwork | A repeatable surface texture | [Image to texture](guides/image-to-texture.md) | [Image to Texture Generator](https://www.playtex.ai/image-to-texture-generator) |
| A prepared surface image | Albedo, normal, roughness, metallic, height, AO, and emission maps | [Image to PBR](guides/image-to-pbr.md) | [PBR Map Generator](https://www.playtex.ai/pbr-map-generator) |
| An existing material texture | A material with reviewed scale, map conventions, and shading | [Material to PBR](guides/material-to-pbr.md) | [PBR Map Generator](https://www.playtex.ai/pbr-map-generator) |
| A scene or lighting idea | A 360° environment panorama | [Skybox generator](guides/skybox-generator.md) | [HDRI Sphere Generator](https://www.playtex.ai/hdri-sphere-generator) |

## ✨ Made with a little texture obsession

<table><tr><td><img src="media/showcase/lava.webp" alt="Actual lava texture output from the PLAYTEX AI image-to-texture walkthrough" width="260"></td><td><img src="media/showcase/black-gold.webp" alt="Black-and-gold material featured on the PLAYTEX AI homepage" width="260"></td><td><img src="media/showcase/basalt.webp" alt="Wet basalt texture featured on the PLAYTEX AI homepage" width="260"></td></tr><tr><td><b>Lava / Image to texture</b></td><td><b>Black & gold / Material inspiration</b></td><td><b>Basalt / Surface detail</b></td></tr></table>

Actual imagery from the PLAYTEX AI website. [See the image-to-texture workflow](https://www.playtex.ai/image-to-texture-generator). Gallery artwork is shown for product illustration; it is not included in the free sample license.

![City-night environment featured on the PLAYTEX AI website](media/showcase/city-night.webp)

**Build the atmosphere, too.** Explore the [skybox generator workflow](guides/skybox-generator.md) and [HDRI Sphere Generator](https://www.playtex.ai/hdri-sphere-generator). This web preview illustrates the environment; it is not a downloadable HDR light probe.

## 🎁 Free asset: a real wood photo, seven PBR maps

[![Real wood-photo source used by PLAYTEX AI](assets/materials/wood-photo/source.png)](https://github.com/playtex-ai/creator-playground/releases/download/v1.1.0/playtex-ai-wood-photo-pbr-512.zip)

**[Download Wood Photo PBR — 512px ZIP](https://github.com/playtex-ai/creator-playground/releases/download/v1.1.0/playtex-ai-wood-photo-pbr-512.zip)** · [Browse files and settings](assets/materials/wood-photo)

A first-party photo crop plus albedo, normal, roughness, metallic, height, AO, and emission maps. Exact PLAYTEX AI reference-core outputs from our published September 2026 example, generated through deterministic image processing. No sign-up for this GitHub download.

Use the pack commercially with attribution under [CC BY 4.0](LICENSE). The source is not seamless or a measured scan. Start emission disabled and review material response in your renderer. [Rights and provenance](RIGHTS.md) · [Checksums](SHA256SUMS.txt). Live-product downloads follow the website’s plan rules.

## 🕹️ Make it yours

Try the **one photo, three moods** challenge: use the wood sample on a prop, then compare warm daylight, cool moonlight, and dramatic side lighting. Keep the material the same and watch the world change. [Share a screenshot](https://github.com/playtex-ai/creator-playground/issues/new/choose) with your renderer and normal-map convention.

Earlier synthetic learning packs remain available in the [v1.0.0 archive](https://github.com/playtex-ai/creator-playground/releases/tag/v1.0.0).

## 📚 Learn the useful bits

- [Engine handoff: Blender, Unity, Unreal, Godot, Three.js, and Roblox](guides/engine-handoff.md)
- [Common questions: free use, PBR maps, seamless textures, and skyboxes](guides/faq.md)
- [Quick map reference and troubleshooting](guides/map-reference.md)
- [PBR export specification and manifest schema](https://github.com/playtex-ai/playtex-pbr-export-spec)
- [Watch the image-to-texture walkthrough](https://www.playtex.ai/watch/image-to-texture-generator)

## What can PLAYTEX AI do with an image?

Use **Image to Texture Generator** to extract a surface from an image with AI assistance and inspect its repeat. Use **PBR Map Generator** to derive material channels from an approved surface through deterministic processing. Use the **HDRI Sphere Generator** for a 360° environment. These are distinct workflows; an ordinary photo is not a complete measured material or a 360° panorama.

## Reuse, cite, or contribute

Maintained by **PLAYTEX AI**. Reviewed September 30, 2026. [Release notes](CHANGELOG.md) · [Citation](CITATION.cff) · [Contributing](CONTRIBUTING.md) · [Versioned releases](https://github.com/playtex-ai/creator-playground/releases).
