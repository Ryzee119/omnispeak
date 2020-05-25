
## Omnispeak: An reimplementation of "Commander Keen in Goodbye Galaxy!"

Omnispeak is an open-source reimplementation of Commander Keen episodes 4, 5, and 6. It aims to be a pixel-perfect, bug-for-bug clone of the original games, and is compatible with savegames from the DOS version.

This Xbox port is a fork of [https://github.com/sulix/omnispeak/](https://github.com/sulix/omnispeak/). A link to this xbox port is here [https://github.com/Ryzee119/omnispeak](https://github.com/Ryzee119/omnispeak).

## Building

Setup and install nxdk. Refer to `https://github.com/XboxDev/nxdk`

Then do this:  
```
export NXDK_DIR=/path/to/nxdk
git clone https://github.com/Ryzee119/omnispeak.git
cd omnispeak
make -f Makefile.nxdk
```
Compiled xbe can be found in `omnispeak/bin/`

**To play, you'll also need to include files from the original game.**  
Omnispeak supports:
* Keen 4 v1.4 EGA
* Keen 5 v1.4 EGA
* Keen 6 v1.4 EGA
* Keen 6 v1.5 EGA

The [Steam version](http://store.steampowered.com/app/9180/) and the [3DRealms](https://3drealms.com/catalog/commander-keen-goodbye-galaxy_8/) version contain Keen4 and Keen5 versions 1.4.  

To get started you can obtain the shareware version of Keen4 for free [here.](https://davidgow.net/keen/omnispeak.html)  
  
Keen 6 is not easily available, infact cannot be purchased legally anywhere. In theory it should work on this Xbox port, but I don't own an original copy of the game so has not been tested.

You'll need to take the following files from your version of Keen, and place them in the `omnispeak/bin/keen_data` folder.  Alternatively place them in `omnispeak/keen_data` before running `make` and they will be copied over automatically and compiled into the xbox .iso.

```
To play Keen4 you need these files:
GAMEMAPS.CK4, EGAGRAPH.CK4, AUDIO.CK4

To play Keen5 you need these files:
GAMEMAPS.CK5, EGAGRAPH.CK5, AUDIO.CK5

To play Keen6 you need these files:
GAMEMAPS.CK6, EGAGRAPH.CK6, AUDIO.CK6
```
