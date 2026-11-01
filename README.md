# Prism — a desktop shell for the CoCo 3 under NitrOS-9

Prism is an original, Finder-style graphical shell for the Tandy
Color Computer 3 running NitrOS-9 Level II: a menu bar, a dithered
colour desktop with drive icons, a mouse pointer, and directory
windows — written from scratch against the standard WindInt
windowing calls, in C (CMOC) with a thin layer of 6809 assembly
system-call wrappers.

**Themes:** Prism Colour (default) and Classic Mono, switchable
live from the View menu — colour is a curated 4-register palette
on the 640x192 screen, with pattern dithering for texture.

## Running it

You need a CoCo 3 (real or emulated) booted into NitrOS-9 Level II
with WindInt — the NitrOS-9 EOU distribution works out of the box.

- From a shell prompt, with `prism` in your CMDS directory: `prism`
- Or from the distribution disk in /D0: `/d0/cmds/prism`

Prism opens its own screen on /W7. Use the mouse (right joystick
port, normal resolution — the standard CoCo mouse setup) to pull
down menus, select drives, and double-click a drive to open its
directory window. Quit from the Prism or File menu, or press `q`.

On exit you land back on the shell screen you started from.

## Building

On a Linux host with CMOC, LWTools and Toolshed on PATH:

    ./build.sh

produces `dist/prism` (the bare OS-9 executable) and
`dist/prism.dsk` (an OS-9 floppy image carrying it).

## Status

v0.1 — see DESIGN.md for what is in, what is planned, and
BUILDLOG.md for how it was built and verified.
