Steam issues on Manjaro Linux
=================

## My Steam doens't load any content

Your Steam only shows menus without any content. And you cann't open Chat windown as well.

It is known issue with `freetype2`, install an update and your Steam will work like a charm.

```bash
sudo pacman -U https://archive.archlinux.org/packages/path/freetype2-2.10.4-1-x86_64.pkg.tar.zst
```

## Last but not least

Swith your input method to English while playing game otherwise you cann't move.
