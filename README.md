# Matplot++ in Unreal Engine

> Refer to [upstream README](https://github.com/alandefreitas/matplotplusplus/blob/master/README.md) for an introduction to Matplot++.

This adds a CMake preset named `plugin` to `CMakePresets.json` for building Maplot++ for use in an Unreal Engine plugin on Windows. The preset prevents mismatches in build type/architecture/toolset/platform between Matplot++ and Unreal Engine that cause _MSB8013_ and _LINK_ errors when building the Unreal Engine project.

Update the generator, toolset, and target platform specified in the `plugin` preset to match what your Unreal Engine version is using. You can then build Matplot++ with the command:
```bash
cmake --preset "plugin"
cmake --build --preset "plugin"
```
and use in Unreal Engine via a [third-party plugin](https://dev.epicgames.com/documentation/en-us/unreal-engine/integrating-third-party-libraries-into-unreal-engine#third-partyplugintemplate).

