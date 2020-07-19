# TF2Classic-Tools
Basic tools for TF2Classic dedicated server development

Also comes with base SourceMod gamedata.

### Usage ###
The main purpose of the this is to remap the natives and forwards that TF2 plugins rely on from the TF2 extension and have them point to the plugin instead. This is because loading the extension on TF2C is impossible without a custom build of SourceMod. To avoid that headache, simply edit and recompile plugins from TF2 (given that they work on TF2C) and they will no longer rely on the TF2 extension.

Just go into the plugin(s) you want to use and change:
```cpp
#include <tf2>
// Or
#include <tf2_stocks>
```
To
```cpp
#include <tf2c>
```

Be aware that a simple recompilation isn't a guaranteed import! TF2Classic does not support certain natives and behaviors that TF2 does.
