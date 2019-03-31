# awesomewm-gnome

Run a GNOME 3.x session but use awesome for window management. At the moment this is only tested on Fedora 29 and a working daily driver Arch Linux system. My latest test was with awesome 4.3 and GNOME 3.32 on March 2019.

If you stumble upon this repo a few years later and I didn't conduct a test in the meantime there are chances that it stopped working, probably because of GNOME.

## Dependencies

The scripts in this repository create a new session in GDM called "awesome GNOME". The requirements are gnome-flashback and awesome 4.3. Earlier versions of awesome don't integrate well with GTK and are sort of buggy.

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

- Works out of the box with all the bells and whistles. 

### The sharp edges

- One thing I noticed with 4.3 is that titlebar rules don't always work, but it is easy to code around that.

- What I also recommend is that your session manager unlocks the GNOME Keyring on login. Otherwise you maybe have the pleasure to enter your password twice or more which can be anoying. See [here](https://wiki.archlinux.org/index.php/GNOME/Keyring#Using_the_keyring_outside_GNOME) to get an idea how to do that.

- If your distro or session manager failes to read or execute anything that you have in your .profile or .xinitrc I would just add that "Feature" myself. It turned out to be extremely handy to have something gets executed no matter what you use in the end. For the nm-applet lovers it could be a more relialable way to launch the applet from one of those files instead of hoping that awesome is doing everything right. The command stayed the same: `dbus-launch nm-applet`

- There is a User report that the files you find here are not working on Ubuntu 18.04 LTS. Until I had the chance to investigate that you are on your own.


