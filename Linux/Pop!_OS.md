# Pop!_OS

Pop!_OS is relatively new and promising Linux distro made by [System76](https://system76.com).

## Installation

1. Download [here](https://system76.com/pop)
2. Decide on going VBox or Live
   1. I recommend live if you have the hardware
3. Follow the install instructions [here](https://pop.system76.com/docs/install-pop-os/)

### Post Install Tips

1. Install [Snap](https://docs.snapcraft.io/t/installing-snap-on-pop-os/11706) for an alternative app store / installer.
  - Be sure to install the Snap Store too: `sudo snap install snap-store`
2. Install exFat format utilities with: `sudo apt-get install exfat-fuse exfat-utils`

## Settings

Any sections omitted are just left with the default settings.

Additionally, if any individual settings are omitted, it's because they haven't been changed from the defaults.

### Appearance

- Background: `Something Dark`
- Lock Screen: `Something Dark`
- Dark Mode: `true`
- Slim Mode: `true`

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
    - Manual from 8pm to 6am
    - Color Temperature: `33%`

## Gnome Tweaks

### Top Bar

- Battery Percentage: `true`
- Clock:
  - Weekday: `true`
  - Date: `true`
  - Seconds: `true`
- Calendar:
  - Week Numbers: `true`

### Window Titlebars

- Titlebar Buttons
  - Maximize: `true`
  - Minimize: `true`

### Windows

- Center New Windows: `true`

### Workspaces

- Display Handling
  - TODO: Find a way to have separate workspace per monitor like macOS does

## Apps

### Install via Pop!_Shop

- Gnome Tweaks
- Spotify

### Install via Snap

**Note:** The shop can be buggy, install these via terminal for the smoothest experience.

- VSCode
- Opera
- Opera Developer Edition

### Install Manually

- Firefox Developer Edition
  - `sudo apt install ubuntu-make`
  - `umake web firefox-dev --lang en-US`
- OBS
  - `sudo apt-get install ffmpeg`
  - `sudo add-apt-repository ppa:obsproject/obs-studio`
  - `sudo apt-get update`
  - `sudo apt-get install obs-studio`

## Resources

- [Pop!_OS Docs](https://pop.system76.com/docs/)
- [Github Repo](https://github.com/pop-os/pop)
- [Snap](https://docs.snapcraft.io/t/installing-snap-on-pop-os/11706)
- Manual Install Guides:
  - [Firefox Dev Edition on Linux](https://www.linuxbabe.com/browser/install-firefox-developer-edition-ubuntu-16-04-linux-mint-18)
  - [VSCode on Linux](https://code.visualstudio.com/docs/setup/linux)
  - [OBS on Linux](https://obsproject.com/wiki/install-instructions#ubuntu-installation)
