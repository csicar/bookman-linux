Bookman Cockpit Linux Edition
=============================

This is a small script that downloads the windows installer from their website, unpacks it, replaces the platform detection and start it up similar to how the `bookman.exe` would do on windows.

Running
-------


```bash
nix run github:csicar/bookman-linux
```


AppImage for non-nix installs
----------------------------

```bash
nix bundle --bundler github:ralismark/nix-appimage github:csicar/bookman-linux
```

DEB Package for debian images
-----------------------------

```bash
nix bundle --bundler github:NixOS/bundlers#toDEB  github:csicar/bookman-linux
```

Update on version changes
-------------------------
When a new version of Bookman is published and you need to rebuild, you must update the flake first:

```bash
nix flake update --flake github:csicar/bookman-linux
```
