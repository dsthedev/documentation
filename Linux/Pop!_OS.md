# Pop!\_OS

Pop!\_OS is one of the best Linux alternatives to Windoze and macOS. Big thanks to [System76](https://system76.com) for creating such an easy to use and flexible operating system!

This document currently uses version `19.10`.

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

```bash
sudo apt update

# Use a Private Window in Firefox first to open docs for reference.
firefox --private-window "https://github.com/dsthedev/documentation"

# First install and configure ZSH
sudo apt install zsh -y
sudo apt install wget git # Required commands
wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | zsh # Download and run installation script
chsh -s /bin/zsh {USER} # Change the default shell to ZSH
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc;
# Logout, login, and ZSH/ohmyzsh should be the default shell!
# gnome-session-quit --force

# Set global git info
git config --global user.name "{USER}"
git config --global user.email "{USER}@{DOMAIN}" # Remember to use githubs private email settings!

# Map a few folders from a backed up drive location to the home folder via symlinks (must be rm -R'd first!)
sudo ln -s /media/{username}/{drive}/documents ~/Documents
sudo ln -s /media/{username}/{drive}/downloads ~/Downloads
sudo ln -s /media/{username}/{drive}/audio ~/Music
sudo ln -s /media/{username}/{drive}/images ~/Pictures
sudo ln -s /media/{username}/{drive}/videos ~/Videos

# Install fonts
(cd ~/Downloads && wget 'https://www.fontsquirrel.com/fonts/download/victor-mono' && wget 'https://www.fontsquirrel.com/fonts/download/source-serif-pro' && wget 'https://www.fontsquirrel.com/fonts/download/source-sans-pro' && wget 'https://www.fontsquirrel.com/fonts/download/source-code-pro')
(cd ~/Downloads; mkdir .fonts; unzip victor-mono -d ~/.fonts/victor-mono; unzip source-serif-pro -d ~/.fonts/source-serif-pro; unzip source-sans-pro -d ~/.fonts/source-sans-pro; unzip source-code-pro -d ~/.fonts/source-code-pro)

# Visual Studio Code
sudo apt install software-properties-common apt-transport-https wget -y # Install dependencies
wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add - # Import Microsoft's GPG key
sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main" # Enable VSCode repository
sudo apt update
sudo apt install code
## Install VSCode extensions

# Neofetch is a handy sysinfo CLI tool
sudo apt install neofetch -y

# These utilities are needed to read & write to exFat drives.
sudo apt install exfat-fuse exfat-utils

# Gnome Tweaks for better customization (Jump to Gnome Tweaks to run all gsettings commands right away)
sudo apt install gnome-tweaks -y

# Spotify for music (Login immediately to start jamming!)
sudo apt install spotify-client -y

# Needed to use Netflix in Firefox
sudo apt install libavcodec-extra -y

# Firefox Developer Edition for web development -- Sign in for sync on first launch!
# THEME: https://addons.mozilla.org/en-US/firefox/addon/animated-blue-plexus/?src=search
(cd ~/Downloads && wget -O firefox-developer-edition-latest.tar.bz2 https://ftp.mozilla.org/pub/devedition/releases/73.0b9/linux-x86_64/en-US/firefox-73.0b9.tar.bz2)
sudo tar -xvf ~/Downloads/firefox-developer-edition-latest.tar.bz2 -C /usr/local/
sudo rm -rf /usr/local/firefox-dev
sudo mv /usr/local/firefox/ /usr/local/firefox-dev/
(cd ~/.local/share/applications/ && curl https://gist.githubusercontent.com/dsthedev/0bba503757a797175184e330e115276f/raw/firefox-dev.desktop --output firefox-dev.desktop --silent)

# Brave for default browser (https://brave-browser.readthedocs.io/en/latest/installing-brave.html)
sudo apt install apt-transport-https curl
curl -s https://brave-browser-apt-release.s3.brave.com/brave-core.asc | sudo apt-key --keyring /etc/apt/trusted.gpg.d/brave-browser-release.gpg add -
echo "deb [arch=amd64] https://brave-browser-apt-release.s3.brave.com/ stable main" | sudo tee /etc/apt/sources.list.d/brave-browser-release.list
sudo apt update; sudo apt install brave-browser -y

# Tor for private browsing (AnonSurf via KaliTools later)

# Opera for personal (and Developer Edition for VPN) -- Sign in for sync on first launch!
wget -qO- https://deb.opera.com/archive.key | sudo apt-key add -
sudo add-apt-repository "deb [arch=i386,amd64] https://deb.opera.com/opera-stable/ stable non-free"
sudo apt install opera-stable -y
#// Popup window inbetween seems to break second install?
sudo add-apt-repository "deb [arch=i386,amd64] https://deb.opera.com/opera-developer/ stable non-free"
sudo apt install opera-developer -y

# OBS for screen recording / streaming
sudo apt install ffmpeg -y
sudo add-apt-repository ppa:obsproject/obs-studio
sudo apt update
sudo apt install obs-studio -y

# NVM / Node / npm
(cd ~/Downloads && curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash)
# Make sure to copy nvm rules from .bashrc to .zshrc first if using ZSH
nvm install --lts

# Virtual Box
# sudo apt install virtualbox -y # outdated, plus it requires the next 3 lines as fix
# sudo apt install virtualbox-dkms -y
# sudo apt install linux-headers-generic -y
# sudo modprobe vboxdrv # https://bugs.launchpad.net/ubuntu/+source/virtualbox/+bug/1466046
wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] http://download.virtualbox.org/virtualbox/debian $(lsb_release -cs) contrib"
sudo apt update && sudo apt install virtualbox-6.1 -y # Make sure to check which version is latest first!

# Vagrant
# sudo apt install vagrant -y # Probably outdated
# Remember to check latest version number first!
(cd ~/Downloads && VER="2.2.7" && wget https://releases.hashicorp.com/vagrant/${VER}/vagrant_${VER}_x86_64.deb && sudo dpkg -i vagrant_${VER}_x86_64.deb && sudo apt -f install)

# Composer
sudo apt install curl php-cli php-mbstring git unzip -y # Dependencies
(cd ~ && curl -sS https://getcomposer.org/installer -o composer-setup.php && sudo php composer-setup.php --install-dir=/usr/local/bin --filename=composer)

# Homestead (for Laravel project development)
vagrant box add laravel/homestead
## Global Homestead folder for reference
git clone https://github.com/laravel/homestead.git ~/Homestead
cd ~/Homestead && git checkout release && bash init.sh
## Install Homestead per project:
cd path/to/project && composer require laravel/homestead --dev && php vendor/bin/homestead make
## Laravel Boilerplate (http://laravel-boilerplate.com)?

# Local by Flywheel (MAMP Alternative for WordPress ONLY)
(cd ~/Downloads && wget -O local-by-flywheel-latest.deb https://local-by-flywheel-flywheel.netdna-ssl.com/latest/linux/deb)
com.github.donadigo.eddy ~/Downloads/local-by-flywheel-latest.deb

# Typora
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys BA300B7755AFCFAE
sudo add-apt-repository 'deb https://typora.io ./linux/'
sudo apt update
sudo apt install typora

# Katoolin for all Kali Linux hacking tools (Steps 1,2, & 4)
(cd ~/Downloads && sudo apt install python git && sudo add-apt-repository universe && git clone https://github.com/LionSec/katoolin.git && sudo cp katoolin/katoolin.py /usr/bin/katoolin && sudo chmod +x /usr/bin/katoolin && sudo katoolin)

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

## Enable Extensions
gsettings set org.gnome.shell disable-user-extensions false

### Dash to Panel (Manual install via browser extension for now)
firefox --private-window "https://extensions.gnome.org/extension/1160/dash-to-panel/"
# git clone https://github.com/home-sweet-gnome/dash-to-panel.git ~/Downloads/dash-to-panel
# (cd ~/Downloads/dash-to-panel && make install) # Doesn't Work!

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
