# DPF-Plugins

Modified for headless plugin build for [Elk Audio OS](https://elk.audio)

## Building Instructions

1. Set up the cross-compilation toolchain with:  

   ```bash
   $ unset LD_LIBRARY_PATH
   $ source /opt/elk-sika64-sdk/environment-setup-aarch64-elk-linux
   ```

2. (optional) Add flags for more aggressive optimizations than the default ones from the toolchain with:  

   ```bash
   $ export CXXFLAGS="-O3 -pipe -ffast-math -felimnate-unused-debug-types"
   ```

3. Finally cross compile the plugin using:  

   ```bash
   $ make plugins
   ```

## Additional notes

* Only the vst plugins have been tried on the Elk Pi.
* Make sure that you update the submodules before trying to build.
* For further compilation help. Look at our [documentation](https://github.com/elk-audio/elk-docs/blob/master/documents/building_plugins_for_elk.md).