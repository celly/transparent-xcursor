# Transparent (hidden) cursor for Gnome / Wayland

#### Why?

While trying to hide cursors for a kiosk in the latest Raspbian Buster, all my old tricks didn't work. This was mainly due to it using Wayland. Wayland doesn't have the `-nocursor` option that X does.

Any hoo, I have never loved the old solutions I used anyways, since they requires addition software (unclutter) or, moving the mouse to 0,0 (which left 1 px showing).. Or, adding in some css, which chromium seems to break on occasion.

#### How?

Download the `transparent` file and overwrite any pointer file you want to hide. In the case of Wayland on Buster that file is:

```
/usr/share/icons/Adwaita/cursors/left_ptr
```

This file was generated with the `xcursorgen` command. You can duplicate the creation by running:

```
xcursorgen transparent.cfg transparent
```

or, in the case of the `left_ptr` file:

```
xcursorgen transparent.cfg left_ptr
```
