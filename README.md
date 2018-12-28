# awesomewm-gnome (WIP)
Run a GNOME 3 session but replace the standard window manager with awesome. At the moment this is only tested on Fedora 29 but if everything goes well this will work on Arch Linux and Ubuntu-likes soon

## Dependencies
This repo creates a new session in GDM called "awesome + Gnome". The requirements are gnome-flashback and awesome 4.x+.

Because gnome-flashback isn't always packaged you might need grab a copy of it from somewhere. Below you can find packages and repositories that worked for me.

# Fedora 29
```
dnf copr enable victoroliveira/gnome-flashback
dnf install gnome-flashback
```

## Installation

```
make install
```

## Uninstallation

```
make uninstall
```

## Configuration

**WIP** 

But it shouldn't be too different from the i3 version just written in lua. Be sure to checkout the extended FAQ as well to make sure all services are running!

> Everything should work out of the box. If you like to use nm-applet add `exec --no-startup-id dbus-launch nm-applet` to your i3 config file.
