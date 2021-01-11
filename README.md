# awesomewm-gnome

Run a GNOME 3.x session but use awesome for window management. 

Unfortunately, I don't use awesome anymore as my daily driver and GNOME tends to break things from time to time so there is a chance this may work on your system or not all. But if you have for example fixes or enhancements feel free to send a PR, I will test and verify those and I will merge them.

My latest test was with **awesome 4.3-2 (Build Date: 31 Jul 2020)** and **GNOME 3.36.6** on **September 2020**.

## Awesome Contributors that kept this Repository alive

Without the people on this list this Project would probably not work at all *and will eat your lunch.*

- [molysgaard](https://github.com/molysgaard)

## Dependencies

The scripts in this repository create a new session in GDM called "awesome GNOME". The requirements are gnome-flashback and awesome 4.3. Earlier versions of awesome don't integrate well with GTK and are sort of buggy.

Because gnome-flashback isn't always packaged you might need grab a copy of it from somewhere. Below you can find packages and repositories that worked for me.

### Arch Linux / Manjaro

```sh
sudo pacman -Syu gnome-flashback gnome gnome-icon-theme gnome-icon-theme-extra
```

### Fedora 29

```sh
dnf copr enable victoroliveira/gnome-flashback
dnf install gnome-flashback
```

### Ubuntu 18.04

```sh
sudo apt-get install gnome gnome-flashback gnome-icon-theme gnome-themes-extra make
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

### The sharp edges

- What I recommend is that your session manager unlocks the GNOME Keyring on login. Otherwise you maybe have the pleasure to enter your password twice or more which can be anoying. See [here](https://wiki.archlinux.org/index.php/GNOME/Keyring#Using_the_keyring_outside_GNOME) to get an idea how to do that.

- There is a User report that the files you find here are not working on Ubuntu 18.04 LTS. Until I had the chance to investigate that you are on your own. 


