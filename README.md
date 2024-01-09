# Platypus

This is a re-assemblable MASM source file for the game code of the 2002 game [Platypus](https://en.wikipedia.org/wiki/Platypus_(video_game)). To be used with [my Blitz3D fork](https://github.com/namazso/blitz3d_msvc2017).

Compile:

```
ml /c bbgame.asm
gcc.exe -s -shared -e_DllEntry -nodefaultlibs -nostdlib bbgame.obj runtime.dll -o bbgame.dll
```

Define `PATCHES=1` for additional patches:

- All resources are loaded on every level, so lightning works on Level 1 too
- Added new cheat: ALT+5 -> Lightning
