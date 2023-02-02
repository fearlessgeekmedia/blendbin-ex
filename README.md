# blendbin-ex
This is a script for exporting binaries which are ran from the command line in Linux containers under [BlendOS](https://github.com/blend-os/blendOS).

This is different from `distrobox-export --app` or `blend export` because those look at the application launchers for the desktop. This script is for command line utilities which wouldn't have desktop launchers. 

This is meant to be used within the container itself, and not on the host system. 

Basic usage:

`blendbin-ex [ name_of_binary ]`

Example

`blendbin-ex yad`

This automatically puts a link into `~/.local/bin` on the host system.

I've written this script to be used in [BlendOS](https://github.com/blend-os/blendOS), though it's very easy to use this on other distros when using [Distrobox](https://github.com/89luca89/distrobox). It just needs to be installed in any Linux container which is made by [Distrobox](https://github.com/89luca89/distrobox).
