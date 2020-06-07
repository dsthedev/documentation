# Pop!\_OS

**Pop!_OS 20.04 LTS**

In my opinion, Pop!\_OS is easily the best alternative to Microsoft's Windows and Apple's macOS operating systems.  I have a ton of respect and admiration for the folks at [System76](https://system76.com) for creating such an easy to use and flexible operating system!

- **Contents:**
- [Installation](#installation)
- [System Preferences](#system-preferences)
- [Gnome Tweaks](#gnome-tweaks)
- [Resources](#resources)
- [TODO](#todo)

---

## Installation

1. Download the iso [here](https://system76.com/pop)
2. Follow the install instructions [here](https://pop.system76.com/docs/install-pop-os/)

### Post Install Recommendations

#### Applications

Before running the commands below and setting up the rest of the system, I recommend following my [Firefox Browser Setup Guide](https://github.com/dsthedev/documentation/blob/master/Setup%20Guides/Firefox.md) to have a well tuned browser ready for any immediate R&D.

```bash
sudo apt update -y

# Neofetch is a handy sysinfo CLI tool
sudo apt install neofetch

# These utilities are needed to read & write to exFat drives.
sudo apt install exfat-fuse exfat-utils

# Gnome Tweaks for better customization
sudo apt install gnome-tweaks -y

# Spotify for music
sudo apt install spotify-client

# Needed to use Netflix in Firefox
sudo apt install libavcodec-extra

# Visual Studio Code
sudo apt install software-properties-common apt-transport-https wget -y # Install dependencies
wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add - # Import Microsoft's GPG key
sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main" # Enable VSCode repository
sudo apt update
sudo apt install code

# Firefox Developer Edition
(cd ~/Downloads && wget -O firefox-developer-edition-latest.tar.bz2 https://ftp.mozilla.org/pub/devedition/releases/78.0b3/linux-x86_64/en-US/firefox-78.0b3.tar.bz2)
sudo tar -xvf ~/Downloads/firefox-developer-edition-latest.tar.bz2 -C /usr/local/
sudo rm -rf /usr/local/firefox-dev
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

# Local by Flywheel (MAMP Alternative for WordPress)
(cd ~/Downloads && wget -O local-by-flywheel-latest.deb https://local-by-flywheel-flywheel.netdna-ssl.com/latest/linux/deb)
com.github.donadigo.eddy ~/Downloads/local-by-flywheel-latest.deb

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
