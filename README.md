# GPUStableFluids
<p align="center">
  <kbd>
    <img src="https://github.com/matthiasbroske/GPUStableFluids/assets/82914350/cb2b031c-8d24-45a1-bf07-79ba8a6b314f" alt="3D Stable Fluids"/>
  </kbd>
</p>
<p align="center">
  <kbd>
    <img src="https://github.com/matthiasbroske/GPUStableFluids/assets/82914350/9ef14477-890a-46f2-ac40-45e535146055" alt="2D Stable Fluids"/>
  </kbd>
</p>

## About
2D and 3D GPU implementations of Jos Stam's infamous [Stable Fluids](https://pages.cs.wisc.edu/~chaol/data/cs777/stam-stable_fluids.pdf) paper using compute shaders in Unity. 
- For the 2D implementation see [`StableFluids2D.cs`](Packages/com.matthiasbroske.gpustablefluids/Runtime/Scripts/StableFluids2D.cs) and [`StableFluids2D.compute`](Packages/com.matthiasbroske.gpustablefluids/Runtime/Compute/StableFluids2D.compute).
- For the 3D implementation see [`StableFluids3D.cs`](Packages/com.matthiasbroske.gpustablefluids/Runtime/Scripts/StableFluids3D.cs) and [`StableFluids3D.compute`](Packages/com.matthiasbroske.gpustablefluids/Runtime/Compute/StableFluids3D.compute), as well as [`Volume.shader`](Packages/com.matthiasbroske.gpustablefluids/Runtime/Shaders/Volume.shader) for the custom shader responsible for volume rendering the 3D fluid.

## Usage
Everything lives in the embedded package [`com.matthiasbroske.gpustablefluids`](Packages/com.matthiasbroske.gpustablefluids) (assembly `MatthiasBroske.GPUStableFluids`). To use it in another project, copy that folder into the project's `Packages/` folder or reference it with a `file:` path in `Packages/manifest.json`.

Download this repository, open with Unity 2022.3 or later, and proceed to either of the two demo scenes in the `Packages/com.matthiasbroske.gpustablefluids/Runtime/Demo/Scenes` folder. The scenes and their respective controls are as follows:
#### `Demo/Scenes/2D Stable Fluids`
2D Stable Fluids simulation rendered directly to the screen.
- **Left Click**: Stir fluid
- **Right Click**: Add dye
- **R**: Reset simulation
#### `Demo/Scenes/3D Stable Fluids`
3D Stable Fluids simulation rendered inside the bounds of a cube.
- **Left Click**: Rotate camera
- **Right Click**: Zoom camera
- **R**: Reset simulation
