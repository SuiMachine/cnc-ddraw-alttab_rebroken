# cnc-ddraw-alttab-rebroken
This is a fork of cnc-ddraw. The purpose of this fork is to re-introduce "build anywhere glitch" of Red Alert 2 (1.0 and 1.0001) that is fixed due to better window handling in cncdraw. There rest is unchanged.
cnc-ddraw can fix compatibility issues in older games, such as black screen, bad performance, crashes or defective Alt+Tab.

&nbsp;

### Features

 - Supports Windows XP, Vista, 7, 8, 10, 11 and Wine
 - GDI / OpenGL / Direct3D 9 renderer (With automatic renderer selection)
 - Upscaling via glsl shaders - https://imgur.com/a/kxsM1oY | https://imgur.com/a/wjrhpFV
 - Windowed Mode / Fullscreen Exclusive Mode / Borderless Mode
 - Alt+Enter support to switch quickly between Fullscreen and Windowed mode
 - Automatically saves and restores window position/size/state
 - FPS Limiter
 - VSync
 - Optional mouse sensitivity scaling
 - Preliminary libretro shader support - https://github.com/libretro/glsl-shaders
 - ...
 
&nbsp;

### Instructions

1. Download [cnc-ddraw.zip](https://github.com/CnCNet/cnc-ddraw/releases/latest/download/cnc-ddraw.zip) and extract it into your game folder
2. Wine only: override `ddraw` in [winecfg](https://wiki.winehq.org/Winecfg#Libraries)
3. Start the game


Note: If you use cnc-ddraw with a game that got its own windowed mode built in then **make sure you disable the games own windowed mode** first.

If you want to play in windowed mode then start the game once in fullscreen and then press Alt+Enter to enable the cnc-ddraw windowed mode (Or enable windowed mode in the config program without using Alt+Enter).

&nbsp;

**If the game starts but it doesn't work perfectly** then open the config program and check the **Compatibility settings**. Alternatively you can also open ddraw.ini with notepad and modify the **Compatibility settings** in there.

&nbsp;

**Compatibility settings in ddraw.ini**

- If there are **problems on Alt+Tab** then try to set `noactivateapp=true` - If it still doesn't work also try `renderer=opengl` or `renderer=gdi`.

- If the **game is running too fast** then try to set `maxgameticks=60` - If it's still too fast, try a lower value.

- If **windowed mode or upscaling are not working properly** then try to set `hook=2` and `renderer=gdi`. 

- If **videos or other UI elements are invisible** then try to set `nonexclusive=true`.

- If some parts of the screen are **being displayed diagonally** then try to set `fixpitch=true`.

- If the game is **stuttering on a Freesync/G-Sync monitor** then try to set `minfps=-1`.

&nbsp;

**If the game doesn't start at all or it's crashing**, [then please generate a debug log file and upload it.](https://github.com/CnCNet/cnc-ddraw/issues/44)  

&nbsp;

### Hotkeys
* [Alt] + [Enter]                  = Switch between windowed and fullscreen mode
* [Ctrl] + [Tab]                    = Unlock cursor
* [Right Alt] + [Right Ctrl]  = Unlock cursor

&nbsp;

### Supported Games

 - Command & Conquer: Red Alert 2

There are a lot more games supported but I don't usually update the list, just give it a try and if it doesn't work then check the instructions above.


[![](https://img.shields.io/github/downloads/cncnet/cnc-ddraw/total)](https://github.com/CnCNet/cnc-ddraw/releases)
