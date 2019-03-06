# Linux Mint Notes

Version 18.3 'Sylvia'
"Cinnamon 64-Bit"

## Installation

- [ ] [Download ISO Image](https://www.linuxmint.com/mirrors.php)
    - Pick a stable and trusted source, I prefer [Harvard's](http://mirrors.seas.harvard.edu/linuxmint/)
- [ ] [Verify Image Integrity](https://linuxmint-installation-guide.readthedocs.io/en/latest/verify.html#download-the-sha256-sums-provided-by-linux-mint)
    - `sha256sum -b yourfile.iso`
- [ ] Proceed to [First Steps](#first-steps) section below

## First Steps

- [ ] Create notes on setup / configuration of system
    - Use Xed (Change to Dark Theme)
- [ ] Connect to Wi-Fi / Ethernet
- [ ] Lightly go through each entry on the "Welcome Screen"
- [ ] Update Drivers
    - Don't switch to proprietary drivers if the device is running fine!
- [ ] Install multimedia codecs if the device is going to be used for multimedia at all
- [ ] Login or sign up for the official forums
- [ ] Install / Remove Languages
    - I prefer to remove any unused languages
- [ ] Setup a system snapshot [Intructions](https://linuxmint-installation-guide.readthedocs.io/en/latest/timeshift.html#system-snapshots)
    - I prefer a weekly schedule
- [ ] Briefly review the [Troubleshooting Guide](https://linuxmint-troubleshooting-guide.readthedocs.io/en/latest/)
- [ ] Download and review the [User Guide](https://www.linuxmint.com/documentation/user-guide/)
- [ ] Consider getting involved in the Linux Mint community, as well as donating 
- [ ] Either continue on to [System Settings](#system-settings) below or start using Mint!

### System Settings

- Appearance
    - Backgrounds - Set a cool looking dark background
    - Effects - Disable all effects
    - Themes - Dark everything
        - Settings - Enable all
- Workspaces
    - Allow cycling through workspaces: `on`

### Software Management

A list of Apps I recommend installing.

- Sublime Text 3
    - If it's outdated, try this: ```bash
wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
sudo apt-get install apt-transport-https
echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list
sudo apt-get update
sudo apt-get install sublime-text```
- Spotify
- Steam
- Chromium Browser
- Bleachbit
- Filezilla
- Blender


### Applets

A list of Applets I recommend downloading and using.

- System Monitor
- Redshift

## Configuration

### Firefox

- Downloads
    - Always ask where to save files
- Default Search Engine
    - DuckDuckGo
- Forms & Passwords
    - Set a short master password
- History
    - Use custom settings:
        - Keep cookies until Firefox is closed
        - Clear history when Firefox closes
- Address Bar
    - Disable history and open tabs
- Tracking Protection
    - Always on
    - Always send a "Do Not Track" signal


## Tips

### Shortcuts

- `Super` - Opens Desktop Menu
- `Ctrl+Alt+Left/Right` Cycle through workspacess

## Resources

- [User Guide](https://www.linuxmint.com/documentation/user-guide/)
- [Installing WordPress on Linux Mint for Development](https://mendo.zone/web/installing-wordpress-on-linux-mint/)

## TODO

- [ ] Thoroughly read all of the documentation for Linux Mint
- [ ] Study the entire User Guide
