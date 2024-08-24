# xdg_popup_crasher

Simple test program to demonstrate a race condition with xdg-popups and the wlr-foreign-toplevel protocol. What this does is trigger the closing of an xdg-popup at the same time while setting it as the location of `zwlr_foreign_toplevel_handle_v1::set_rectangle` for another view. See [here](https://github.com/WayfireWM/wayfire/issues/2445) for more context.

Compiling (requires the Wayland client libraries, cairo and EGL interface to be installed):

```
meson build
ninja -C build
```

Running:

```
build/wlrc
```


