# awesomewm-gnome

Run a GNOME 3 session but use awesome as your window manager. At the moment this is only tested on Fedora 29 and Arch Linux but if everything goes well this will work Ubuntu-likes soon.

## Dependencies

The scripts in this repository create a new session in GDM called "awesome GNOME". The requirements are gnome-flashback and awesome 4.x+. I recommend building awesome from git to avoid some nasty bugs and to support GTK 3 in your Themes.

Because gnome-flashback isn't always packaged you might need grab a copy of it from somewhere. Below you can find packages and repositories that worked for me.

### Arch Linux

```sh
sudo pacman -Syu gnome-flashback gnome gnome-icons gnome-icons-extra
```

### Fedora 29

```sh
dnf copr enable victoroliveira/gnome-flashback
dnf install gnome-flashback
```

## Setup

Run the following with if you have sudo installed

```sh
sudo make install
```

## How to uninstall

```sh
sudo make uninstall
```

## Configuration

Works out of the box with all the bells and whistles. 

You might want to install a bleeding edge version of awesome and use the new GTK features for your theme.

~~Like in the original i3 version if you want the `nm-applet` you have to launch from your config.~~
You will need some more code to make sure there is only one nm-applet.

```lua
awful.spawn("dbus-launch nm-applet", false) -- Launch nm-applet without startup id
```
