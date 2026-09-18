# Personal st build

This repository is a personalized build of st based on the official suckless
history. See `PATCHES.md` for the integrated alpha, HarfBuzz, and emoji changes.

## Dependencies

- Xlib, Xft, Fontconfig, and FreeType development files
- HarfBuzz development files
- Noto Color Emoji

On Debian:

```sh
sudo apt install build-essential libx11-dev libxft-dev libfontconfig-dev \
  libfreetype-dev libharfbuzz-dev fonts-noto-color-emoji
```

## Build and install

```sh
make
sudo make install
```

New st processes use the installed binary; existing terminals do not need to
be restarted.

The official upstream should be configured as the `upstream` remote; reserve
`origin` for the personal GitHub repository.
