# Skybox generator: create a 360° environment and prepare it for your scene

**A skybox generator creates environment imagery surrounding a 3D scene.** PLAYTEX AI's HDRI Sphere Generator supports AI-assisted 360° panorama creation. Preparing that panorama as six cubemap faces is a separate, deterministic projection step.

[Open HDRI Sphere Generator](https://www.playtex.ai/hdri-sphere-generator) · [Panorama to Cubemap Converter](https://www.playtex.ai/tools/panorama-to-cubemap-converter) · [Roblox skybox workflow](https://www.playtex.ai/roblox-skybox-generator)

## Start with a coherent scene

Describe the setting, time of day, horizon, and lighting direction together. For example: “A stylized desert plateau at dusk, peach light near the horizon, violet upper sky, distant silhouettes, open space in every direction.” Review the result all the way around; the first attractive camera view does not establish that the complete panorama works.

## The workflow

1. Open HDRI Sphere Generator and use the available prompt or image-guided workflow.
2. Generate and inspect the 360° result, including the horizontal wrap, both poles, horizon height, and repeated landmarks.
3. Decide whether your destination expects an equirectangular panorama or six square faces.
4. Export the available result. If needed, use Panorama to Cubemap Converter to prepare the required projection.
5. Check face order, rotations, color space, and exposure in your target application. Roblox uses a dedicated skybox workflow; do not assume all generic face sets can be uploaded unchanged.

## Free example: Apricot Orbit

![Apricot Orbit panorama](../media/apricot-orbit-panorama.png)

[Download the skybox](../downloads/apricot-orbit-skybox.zip). It contains a 2048 × 1024 PNG panorama, six 512 × 512 PNG faces, and skybox.json describing the projection and orientation. The panorama is original authored artwork; the faces are actual PLAYTEX AI projection-core outputs. This sample demonstrates packaging and projection, not AI generation quality.

The generic face filenames are px, nx, py, ny, pz, nz. That is the array order expected by [Three.js CubeTextureLoader](https://threejs.org/docs/pages/CubeTextureLoader.html). Confirm the renderer's coordinate system and orientation in a scene rather than relying on filenames alone.

## Skybox, panorama, and HDRI are not synonyms

- **Skybox** describes how environment imagery is used around a scene.
- **Equirectangular panorama** describes a latitude/longitude image layout, commonly 2:1.
- **Cubemap** describes six square image faces representing directions.
- **High dynamic range** describes the range of stored light values, not whether an image is panoramic.

The downloadable Apricot Orbit PNGs are **LDR/display-referred backgrounds**. Converting a PNG to six faces or saving it in another container does not recover measured HDR illumination. Judge lighting separately from the visible background.

Reviewed by PLAYTEX AI, September 30, 2026. [All guides](README.md)
