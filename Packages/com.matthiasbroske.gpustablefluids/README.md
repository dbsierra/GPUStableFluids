# GPU Stable Fluids

2D and 3D GPU implementations of Jos Stam's [Stable Fluids](https://pages.cs.wisc.edu/~chaol/data/cs777/stam-stable_fluids.pdf) using compute shaders in Unity.
Original project: [matthiasbroske/GPUStableFluids](https://github.com/matthiasbroske/GPUStableFluids).

Requires Unity 2022.3+ and URP.

## Install
Copy this folder into your project's `Packages/` folder, or add it to `Packages/manifest.json`:
```json
"com.matthiasbroske.gpustablefluids": "file:<path-to>/com.matthiasbroske.gpustablefluids"
```

## Contents
- `Runtime/Scripts` – `StableFluids2D`, `StableFluids3D`, `RenderTextureUtilities` (namespace `StableFluids`, assembly `MatthiasBroske.GPUStableFluids`)
- `Runtime/Compute` – simulation compute shaders
- `Runtime/Shaders/Volume.shader` – volume raymarching shader (`MatthiasBroske/GPUStableFluids/Volume`)
- `Runtime/Materials`, `Runtime/Textures/Colormaps` – default volume material and colormaps
- `Runtime/Demo` – demo scenes, `OrbitCam`, test images

## Demo scenes
#### `Runtime/Demo/Scenes/2D Stable Fluids`
- **Left Click**: Stir fluid
- **Right Click**: Add dye
- **R**: Reset simulation
#### `Runtime/Demo/Scenes/3D Stable Fluids`
Enable **Depth Texture** on the URP asset/camera.
- **Left Click**: Rotate camera
- **Right Click**: Zoom camera
- **R**: Reset simulation

Note: the components read input through the legacy `Input` API, so the project's Active Input Handling must be "Input Manager" or "Both".
