# Windoze Installation

_Last updated_: **2019-12-07**

**Note**: I pretty much only use Windows for PC gaming, so that's what this guide is tailored to.

## Pre-Install Process

1. Download the Windows 10 Disc Image (ISO File) from `microsoft.com` [here](https://www.microsoft.com/en-us/software-download/windows10ISO)
   1. **Note**: If you're on Windows already, it will redirect you to their installation tool; to get around this spoof your device type using browser developer tools.
2. Download and run [Rufus](https://rufus.ie/)
   1. Select a 8GB+ USB for the device, the downloaded Windoze ISO for Boot selection, and press start to create the bootable installer.
3. Put bootable USB installer in computer and boot into it

---

## Installation Options

1. "I don't have a product key"
2. Windows 10 Pro (because RDP and cleaner overall)
3. Accept license after reading
4. Choose "Custom: Install Windows only (advanced)"
5. Format drives appropriately
6. _Optional_: Get coffee while waiting for Windoze 10 to install
7. Choose your region
8. Select keyboard layout
9. Skip secondary keyboard layout
10. Set usage type to personal
11. Select "offline account"
12. Make Commander admin account / password
    1. Ugh, also set 3 security questions
13. Disable activity history
14. Decline Cortana assistance
15. Disable all "privacy settings"
16. _Optional_: Get more coffee while waiting more for Windoze to setup

---

## Post Install Process / Customize

1. Download and run my [Windows 10 Setup Powershell Script](https://gist.githubusercontent.com/dsthedev/4ab9662546ad0d984d0dfacddc88117f)
2. Follow my old instructions from before:

```markdown
- Taskbar
	- Remove all app shortcuts
	- Set volume to 80%
- Start Menu
	- Settings
		- Hide app list
		- Hide recently used
		- Don't show suggestions
		- Don't show recently opened items in jump list on start or taskbar
		- Chosen folders to show: All off except for settings & personal folder
	- Tiles - Turn live tile off and/or Uninstall everything except for:
		- Weather
		- Edge
		- Network Speed Test
		- Alarms
		- Calculator
		- Remote Desktop Connection
- Quick Access - Unpin Desktop, Downloads, and Pictures
	- Add relevant folders and drives like X: or htdocs
- Windows Settings (New Interface)
  - System
    - Display
      - Enable Night Light at ~50%
      - Enable schedule (sunset to sunrise)
    - Notifications
      - Disable all except "From apps and other senders", Edge, Security/Maintenance, and user installed apps
    - Storage
      - Enable Storage sense
    - Multitasking
      - Disable automatic window sizing to available space
      - Disable showing what can snap next to snapped window
      - Disable resizing of adjacent window
    - Shared Experience - disable
  - Network
    - Set static IP
      - Use `ipconfig` to find IP
      - Network and Sharing -> Change adapter settings -> Ethernet properties
      - Internet Protocol Version 4 (TCP/IPv4) -> Properties
      - Apply settings from ipconfig, or custom IP
  - Personalize
    - Cool background & lock screen
    - Darkest color theme
    - Disable "tips" on lock screen
    - Inverted mouse theme
  - Privacy - Turn off everything except notifications
- Other settings, configurations, and general tweaks
  - Disable onedrive, set to not start on login, and exit
- Configure Edge Settings
  - Dark theme
  - Open Edge with `about:blank`
  - Open new tabs with blank page
  - Clear all browsing data and set Always clear when browser closes to on
  - Advanced
    - Hide home button
    - Disable Adobe Flash Player
    - Change download folder to `E:\Downloads` and make sure "Ask what to do each time" is enabled
    - Disable password saving
    - Disable form entry saving
    - Enable sending "Do Not Track" requests
    - Disable Cortana assistance
    - Visit google.com at least once and set it as the default search engine
    - Don't show search history
    - Don't show frequently visited sites
    - Disable page prediction
```

---

## Reference Images

### Pre-Install Process Images

![Windoze 10 Download](./images/windoze-10-dl_01.png)

![Rufus Install](./images/rufus-win10_03.png)

### Installation Options Images

![01 - "I don't have a product key"](./images/installation/01-activate-windows.png)

![02 - Windows 10 Pro (because RDP and cleaner overall)](./images/installation/02-os-type.png)

![03 - Accept license after reading](./images/installation/03-accept-license.png)

![04 - Choose "Custom: Install Windows only (advanced)"](./images/installation/04-install-type.png)

![05 - Format drives appropriately](./images/installation/05-format-drives.png)

![06 - *Optional*: Get coffee while waiting for Windoze 10 to install](./images/installation/06-get-coffee.png)

![07 - Choose your region](./images/installation/07-region.png)

![08 - Select keyboard layout](./images/installation/08-keyboard-layout.png)

![09 - Skip secondary keyboard layout](./images/installation/09-skip-second-layout.png)

![10 - Set usage type to personal](./images/installation/10-usage-type.png)

![11 - Select "offline account"](./images/installation/11-create-offline-account.png)

![12 - Make Commander admin account / password](./images/installation/12-make-commander-admin.png)

![13 - Disable activity history](./images/installation/13-disable-activity-history.png)

![14 - Decline Cortana assistance](./images/installation/14-decline-cortana.png)

---

## Helpful Resources

### Powershell Resources

- [Richard's Powershell Blog](https://richardspowershellblog.wordpress.com/)

### Font Resources

- [Victor Mono](https://www.fontsquirrel.com/fonts/victor-mono)
- [Source Serif Pro](https://www.fontsquirrel.com/fonts/source-serif-pro)
- [Source Sans Pro](https://www.fontsquirrel.com/fonts/source-sans-pro)
- [Source Code Pro](https://www.fontsquirrel.com/fonts/source-code-pro)
