# snes9x-xscreensaver

This is a quick and dirty hack of Snes9x that works with XScreenSaver. It plays back Snes9x movie files (`.smv`) at random from the list given. When the movie finishes, it plays another one.

Movie files are not compatible between Snes9x versions. This code is based on Snes9x 1.51 so you'll need `.smv` files created with that version (there are some [here](http://www.freewebs.com/saturnsmovies/snesmovies.htm)).

# Installation

Compile the `xsnesx` binary:

```bash
./configure --with-xss && make
```

Copy it somewhere XScreenSaver can find it (usually `/usr/lib/xscreensaver`):

```bash
 chmod 0755 xsnes9x && sudo cp xsnes9x /usr/lib/xscreensaver
```

Configure XScreenSaver (edit `~/.xscreensaver` or run `xscreensaver-demo`) to run the following command:

```bash
xsnes9x -root -rom /path/to/rom.sfc -movies /path/to/movie.smv,/path/to/other/movie.smv,...
```
