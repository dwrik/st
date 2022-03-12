# st - simple terminal

st is a simple terminal emulator for X which sucks less.

## dwrik's build

This is my build of st (simple terminal) from suckless. This build includes the following patches:

- alpha - enables transparency
- font2 - enables additional font for rendering glyphs
- ligatures - enables proper rendering of ligatures
- xresources - draws in settings from xresources (colors, alpha, font etc.)
- scrollback - enables scrollback on the terminal (no scrollback by default on st)

## Requirements

In order to build st you need the Xlib header files.

## Installation

Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):
```
make clean install
```

## Running st

If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:
```
tic -sx st.info
```

See the man page for additional details.
