# PF2-Tools
Basic tools for Pre-Fortress 2 dedicated server development

Also comes with base SourceMod gamedata.

# New forks

If you are interested in making a version for your own Source Mod, use [this video guide](https://youtu.be/SD6Rn2D7IGo) by the original creator to find the **digital signatures.**

### Usage ###
The main purpose of the this is to remap the natives and forwards that TF2 plugins rely on from the TF2 extension and have them point to the plugin instead. This is because loading the extension on PF2 is impossible without a custom build of SourceMod. To avoid that headache, simply edit and recompile plugins from TF2 (given that they work on PF2) and they will no longer rely on the TF2 extension.

Just go into the plugin(s) you want to use and change:
```cpp
#include <tf2>
// Or
#include <tf2_stocks>
```
To
```cpp
#include <pf2>
```

Be aware that a simple recompilation isn't a guaranteed import! Pre-Fortress does not support certain natives and behaviors that TF2 does.
