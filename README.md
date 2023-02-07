# blendbin-ex
This is a script for exporting binaries which are ran from the command line in Linux containers under [BlendOS](https://github.com/blend-os/blendOS).

This is different from `distrobox-export --app` or `blend export` because those look at the application launchers for the desktop. This script is for command line utilities which wouldn't have desktop launchers. 

This is meant to be used within the container itself, and not on the host system. 

Basic usage:

`blendbin-ex [ name_of_binary ] [ export path (optional)`

Example

`blendbin-ex yad`

Or with the optional export path

`blendbin-ex yad /home/username/somethingelse`

Without the export path, it will abutomatically export to `~/.local/bin` on the host system.

I've written this script to be used in [BlendOS](https://github.com/blend-os/blendOS), though it's very easy to use this on other distros when using [Distrobox](https://github.com/89luca89/distrobox). It just needs to be placed in any Linux container which is made by [Distrobox](https://github.com/89luca89/distrobox).

Chances are, if you're using an immutable distribution, (at least from what I've seen in the immutable distrobutions I've used) you have a `~/.local/bin` folder . This is where the script currently exports the binary too. If you don't have this, at this time you will want to create it. You may not have this folder if you're on a more traditional Linux system, for example. I am strongly considering allowing a second option for a custom export path. But this will be the path by default. 

## To-do
- Add error checking to make sure the binary exported properly -and this should be done soon
