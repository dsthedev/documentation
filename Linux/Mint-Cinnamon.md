# Linux Mint Notes

Version 18.3 'Sylvia'
"Cinnamon 64-Bit"

## Installation

- [ ] [Download ISO Image](https://www.linuxmint.com/mirrors.php)
    - Pick a stable and trusted source, I prefer [Harvard's](http://mirrors.seas.harvard.edu/linuxmint/)
- [ ] [Verify Image Integrity](https://linuxmint-installation-guide.readthedocs.io/en/latest/verify.html#download-the-sha256-sums-provided-by-linux-mint)
    - `sha256sum -b yourfile.iso`
- [ ] Proceed to [First Steps](#first-steps) section below

### Install From USB

Install (as superuser)

- Language: `English`
- Keyboard layout: `English (US)`
- Install third-party software for graphics, wi-fi, etc: `true`
- Erase disk and install Linux Mint
- Where are you?  Enter city/state
- Name: `SuperUser`
- Computer Name: PC name without user name (`OptiPlex-3020M-01`) plus a numerical suffix
- Username: `superuser`
- Password: `root` if you don't care about security, otherwise this should be a very strong password for the super admin!

## First Steps

Do the following as the SuperUser / Admin first.

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
    - I prefer a 1 monthly, 4 weekly, & 7 dailys
- [ ] Briefly review the [Troubleshooting Guide](https://linuxmint-troubleshooting-guide.readthedocs.io/en/latest/)
- [ ] Download and review the [User Guide](https://www.linuxmint.com/documentation/user-guide/)
- [ ] Consider getting involved in the Linux Mint community, as well as donating
- [ ] Either continue on to [System Settings](#system-settings) below or start using Mint!

Before customizing anything, add a Standard user for the person who will be using the computer regularly and most often!

### System Settings

- Appearance
    - Backgrounds - Set a cool looking dark background
    - Effects - Disable all effects
    - Font Selection - Download `Source Sans/Code/Serif Pro` fonts and apply appropriately
    - Themes - Dark everything
        - Settings - Enable all
- Preferences
  - Accessibility
    - Desktop Zoom: `Enable`
      - Mag: `1.0`
      - Mouse wheel modifier: `Alt`
      - Scroll at screen edges: `false`
      - Mouse Tracking mode: `Cursor moves with content`
      - Lens mode: `true`
      - Lens shape: `Horizontal Strip` (or `Square`)
    - Keyboard Indicators
      - Use visual indicator on caps and num lock: `true`
  - Account Details: `@todo`
  - Applets: `@todo`
  - Date & Time
    - Double check the network time & date are correct, if not then unlock and adjust
    - Format: Enable all; 24h clock, display date, display seconds
    - First day of week: `Sunday`
  - Desklets: `@todo`
  - Desktop
    - Desktop Layout: `No desktop icons`
      - Desktop Icons: `Enable all` just in case?
  - Extensions: `@todo`
  - General: Leave at defaults
    - `@todo` look into compositing and other settings such as timer for logout/shutdown
  - Hot Corners: `@todo` find a way to mimic macOS sleep screen in bottom right corner
  - Input Method: Skip, unless you need to enter symbols from foriegn languages
  - Languages
    - Set language and region appropriately, as well as apply a system-wide locale
    - Remove any unnecessary languages
  - Notifications: Leave at defaults
  - Online Accounts: `@todo`
  - Panel: Leave at defaults
  - Preferred Applications: `@todo`
  - Privacy: `@todo`
  - Screensaver: `@todo`
  - Startup Applications: `@todo`
  - Windows: `@todo`
  - Window Tiling: `@todo`
  - Workspaces: `@todo`
    - Allow cycling through workspaces: `on`
- Hardware: `@todo`
  - Bluetooth: `@todo`
  - Color: `@todo`
  - Display: `@todo`
  - Graphics Tablet: `@todo`
  - Keyboard: `@todo`
  - Mouse and Touchpad: `@todo`
  - Network: `@todo`
  - Power Management: `@todo`
  - Printers: `@todo`
  - Sound: `@todo`
  - System Info: `@todo`
- Administration: `@todo`
  - Driver Manager: `@todo`
  - Firewall: `@todo`
  - Login Window: `@todo`
  - Software Sources: `@todo`
  - Users and Groups: `@todo`

### Software Management

#### Included Software

- Firefox: for viewing PDF's

#### Recommended Software

`@todo`: revise this list

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

`@todo`: revise this list

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
