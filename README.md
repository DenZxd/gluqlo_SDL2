# Gluqlo: Fliqlo for Linux (SDL2)

Fork of Gluqlo with SDL2 support. Be sure to set the environment variable `SDL_VIDEO_ALLOW_SCREENSAVER=1` before starting the screensaver background daemon (xscreensaver, etc.). To avoid staggering while the screensaver is running set the **Cycle After** option in `xscreensaver-settings` to 0 minutes.

## Background

Some Linux distros (ie. Arch) have recently replaced the `sdl` package with `sdl12-compat`, which attempts to wrap SDL2 functionality into SDL1.2. gluqlo no longer works as a result because `SDL_WINDOWID` is ignored by sdl12-compat. This environment variable no longer exists in SDL2, and screensaver programs running hacks using SDL1.2 need `SDL_WINDOWID` to properly display. Instead of waiting for sdl12-compat to add support for this environment variable I decided to migrate the gluqlo project to SDL2.



Installing after download tarball or zip:

unpack and go to folder

sudo apt-get install build-essential libsdl1.2-dev libsdl-ttf2.0-dev libsdl-gfx1.2-dev libx11-dev

next:
make && sudo make install

If you have some errors then install this (and another library if you need):
sudo apt update && sudo apt install libsdl2-gfx-dev

then run:
make && sudo make install

best to use this screensaver:
sudo apt update
sudo apt install xfce4-screensaver
