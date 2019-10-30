# Pop!\_OS

Pop!\_OS is one of the best Linux alternatives to Windoze and macOS. Big thanks to [System76](https://system76.com) for creating such an easy to use and flexible operating system!

This document currently uses version `19.10`.

- [Installation](#installation)
- [System Preferences](#system-preferences)
- [Gnome Tweaks](#gnome-tweaks)
- [Resources](#resources)

---

## Installation

1. Download the iso [here](https://system76.com/pop)
2. Follow the install instructions [here](https://pop.system76.com/docs/install-pop-os/)

### Post Install Recommendations

#### Applications

```bash
sudo apt update

# These utilities are needed to read & write to exFat drives.
sudo apt install exfat-fuse exfat-utils

# Gnome Tweaks for better customization
sudo apt install gnome-tweaks -y

# Spotify for music
sudo apt install spotify-client

# Visual Studio Code
sudo apt install software-properties-common apt-transport-https wget -y # Install dependencies
wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add - # Import Microsoft's GPG key
sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main" # Enable VSCode repository
sudo apt update
sudo apt install code

# Firefox Developer Edition (DOESN'T WORK)
# sudo apt install ubuntu-make -y
# umake web firefox-dev --lang en-US

# Firefox Developer Edition
# wget -P ~/Downloads/ https://ftp.mozilla.org/pub/firefox/releases/71.0b4/linux-x86_64/en-US/firefox-71.0b4.tar.bz2 # Add -q to hide progress, downloads regular, not Dev Edition!
# For now, it seems the actual developer edition HAS to be downloaded manually for linux...
# https://www.mozilla.org/en-US/firefox/developer/
sudo tar -xvf ~/Downloads/firefox-*.tar.bz2 -C /usr/local/
sudo mv /usr/local/firefox/ /usr/local/firefox-dev/
(cd ~/.local/share/applications/ && curl https://gist.githubusercontent.com/dsthedev/0bba503757a797175184e330e115276f/raw/firefox-dev.desktop --output firefox-dev.desktop --silent)

# Opera (and Developer Edition)
wget -qO- https://deb.opera.com/archive.key | sudo apt-key add -
sudo add-apt-repository "deb [arch=i386,amd64] https://deb.opera.com/opera-stable/ stable non-free"
sudo apt install opera-stable -y
sudo add-apt-repository "deb [arch=i386,amd64] https://deb.opera.com/opera-developer/ stable non-free"
sudo apt install opera-developer -y

# OBS for screen recording / streaming
sudo apt install ffmpeg -y
sudo add-apt-repository ppa:obsproject/obs-studio
sudo apt update
sudo apt install obs-studio -y

# NVM / Node / npm
(cd ~/Downloads && curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash)
nvm install --lts

# Virtual Box
sudo apt install virtualbox -y

# Vagrant
sudo apt install vagrant

# Composer
sudo apt install curl php-cli php-mbstring git unzip -y # Dependencies
(cd ~ && curl -sS https://getcomposer.org/installer -o composer-setup.php && sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer)

# Typora
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys BA300B7755AFCFAE
sudo add-apt-repository 'deb https://typora.io ./linux/'
sudo apt update
sudo apt install typora
```

If an app doesn't create a desktop link, it will need to be manually created, example:

```conf
# ~/.local/share/applications/firefox-dev.desktop
[Desktop Entry]
Name=Firefox Developer
GenericName=Firefox Developer Edition
Exec=/usr/local/firefox-dev/firefox %u
Terminal=false
Icon=/usr/local/firefox-dev/browser/chrome/icons/default/default128.png
Type=Application
Categories=Application;Network;X-Developer;
Comment=Firefox Developer Edition Web Browser.
```

#### Snapcraft

[Snapcraft](https://snapcraft.io/) is an alternative app store and package manager. It has certain apps that I use regularly that are not on Pop!\_Shop.

```bash
sudo apt update
sudo apt install snapd
sudo snap install snap-store
```

**Note:** The Snap Store may not be available until the machine has been restarted.

##### Snap Apps

These apps can be installed via the Snap Store, but doing it with the command line is faster and easier.

```bash
sudo snap install opera
sudo snap install opera-developer --edge
```

---

## System Preferences

Any sections omitted are just left with the default settings.

Additionally, if any individual settings are omitted, it's because they haven't been changed from the defaults.

### Appearance

- Background: `Something Dark`
- Lock Screen: `Something Dark`
- Dark Mode: `true`
- ~~Slim Mode: `true`~~ Removed in 19.10?!

### Online Accounts

- Link Google account for Mail and Calendar

### Privacy

- Screen Lock
  - Lock screen after blank for: `5 minutes`
- Usage & History: `Disable and Clear`
- Purge Trash & Temporary Files
  - Automatically empty Trash: `true`
  - Automatically empty Temporary Files: `true`
  - Purge After: `7 days`
  - Purge both manually

### Devices

- Displays
  - Night Light: `true`
    - Manual from 7pm to 7am
    - Color Temperature: `33%`

---

## Gnome Tweaks

The default settings (system preferences) are fairly limited; Gnome Tweaks adds some useful options.

```bash
# gnome-tweaks -v

## Top Bar:
gsettings set org.gnome.desktop.interface show-battery-percentage true
gsettings set org.gnome.desktop.interface clock-show-weekday true
gsettings set org.gnome.desktop.interface clock-show-date true
gsettings set org.gnome.desktop.interface clock-show-seconds true
gsettings set org.gnome.desktop.calendar show-weekdate true

## Window Titlebars
gsettings set org.gnome.desktop.wm.preferences button-layout "appmenu:minimize,maximize,close"

## Windows
gsettings set org.gnome.mutter center-new-windows true
gsettings set org.gnome.mutter dynamic-workspaces true
gsettings set org.gnome.mutter workspaces-only-on-primary true
```

---

## Resources

- [Pop!\_OS Docs](https://pop.system76.com/docs/)
- [Github Repo](https://github.com/pop-os/pop)
- [Snap](https://docs.snapcraft.io/t/installing-snap-on-pop-os/11706)
- [Firefox Desktop Downloads](https://www.mozilla.org/en-US/firefox/channel/desktop/)

## TODO

- Create a bash install script to install additional applications and configure system settings.
