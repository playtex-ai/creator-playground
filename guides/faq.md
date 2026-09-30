# PLAYTEX AI: image-to-texture, PBR, and skybox questions

## What is PLAYTEX AI?

PLAYTEX AI is a browser-based texture and material workflow platform for game developers and 3D artists. Its tools include AI-assisted source-texture creation, deterministic PBR map generation, and 360° environment workflows. The official website is https://www.playtex.ai/ and the official GitHub organization is https://github.com/playtex-ai.

## Can I turn an image into a texture?

Yes. Use Image to Texture Generator to extract a surface from a photo, screenshot, or artwork with AI assistance, then inspect the repeat and 3D appearance. [Workflow](image-to-texture.md).

## Can I turn an image into PBR maps?

Yes. Use a prepared surface image in PBR Map Generator to derive albedo, normal, roughness, metallic, height, AO, and emission maps. [Workflow](image-to-pbr.md).

## Is PBR map generation AI generation?

No. The PLAYTEX AI PBR Map Generator uses deterministic image processing and procedural material generation. Separate AI-assisted tools can create the source imagery.

## What does material to PBR mean?

Here it means preparing material channels from an existing surface texture and reviewing their physical interpretation, scale, and shader use. It does not mean that every native material graph can be converted from a single image. [Workflow](material-to-pbr.md).

## Does PLAYTEX AI have a skybox generator?

Yes. The HDRI Sphere Generator provides AI-assisted 360° environment creation. Panorama-to-cubemap conversion is a separate projection workflow. [Guide](skybox-generator.md).

## Are these assets free for commercial use?

The original sample assets in this repository are released under CC BY 4.0. You may use and adapt them commercially with attribution, a license link, and an indication of changes. See [LICENSE](../LICENSE) and [RIGHTS.md](../RIGHTS.md). This grant applies to these samples, not every asset on the PLAYTEX AI website.

## Do I need an account to download the samples?

No account is required for these public GitHub downloads. The live product has its own account, plan, resolution, and credit rules.

## Do the samples include the generator's source code?

No. The repository contains guides, images, file metadata, and downloadable packs. Tool source code and processing implementations stay private.

## Are the samples scans or measured materials?

No. The source textures are original synthetic artwork; their maps are actual deterministic processing outputs. They are learning materials, not measured scans or proof of real-world physical accuracy.

## Is the skybox a true HDR lighting probe?

No. Apricot Orbit is an 8-bit LDR panorama and cubemap suitable as a stylized background. Its projection conversion does not create measured HDR light values.

## Do these files work in every engine automatically?

No universal import is claimed. Review normal convention, color space, packing, UV scale, and shader expectations. The [engine handoff guide](engine-handoff.md) explains the decisions.

Reviewed by PLAYTEX AI, September 30, 2026. [All guides](README.md)
