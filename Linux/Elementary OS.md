# Elementary OS

## OS Install

1. English
2. Connect to WiFi
3. Download updates & install 3rd party drivers
4. Erase disk and install elementary
5. Set time zone to Eau Claire, WI
6. English (US) keyboard
7. Create an admin account (Commander)

After installation and restart, double check for updates.  Sometimes the download updates option fails during installation.

## Basics

- Install Eddy with `sudo apt-get install eddy`
- Install Synergy with Eddy
- Install VSCode with Eddy
- Install git with `sudo apt-get install git`
- [Enable PPA](https://elementaryos.stackexchange.com/questions/7507/how-can-i-add-a-ppa-in-loki) adding with `sudo apt install software-properties-common`
- Follow [Typora's install](http://support.typora.io/Typora-on-Linux/) for linux installation:

```bash
# optional, but recommended
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys BA300B7755AFCFAE

# add Typora's repository
sudo add-apt-repository 'deb https://typora.io ./linux/'
sudo apt-get update

# install typora
sudo apt-get install typora
```

- If it [doesn't run](https://github.com/electron/electron/issues/1518), may need to use `sudo apt-get install libgconf-2-4`
- Clone [Documentation](https://gitlab.com/dsthedev/Documentation) project into `~/Documents`

## Customize

1. Remove Music and Videos from Dock
2. System Settings
   1. Desktop
      1. Cool Dark Background
      2. Small Icons
      3. Hide Dock when focused window overlaps
      4. Hot Corners
         1. Top Left: Show App Menu
         2. Bottom Left: Show all windows
   2. Security & Privacy - Disable OS History
   3. Remove System Settings from Dock
3. Remove App Center from Dock
4. Add Terminal, Typora, and "Files" to Dock

## Apps

- Epiphany
  - General - Don't allow advertisements
  - Privacy
    - Tell websites you don't want to be tracked
    - Don't remember passwords
- Mail - Add account(s)
- Calendar - Add account(s)

## LAMP

- https://www.lifeofgeek.com/install-lamp-elementary-os-loki/

## Keyboard Shortcuts

- Switch desktop:`cmd + left / right`
- Switch desktop alt: `cmd + tab, (+ shift to reverse)`
- Maximize window: `cmd + up`
- Active App view: `cmd + down`
- Resize window to left / right half: `ctrl + cmd + left / right`
- Move window to another desktop: `cmd + option + left / right`

## Troubleshooting

- Can't update OS?  `sudo apt update && sudo apt upgrade`