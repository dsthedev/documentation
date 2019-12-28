# New Mac Notes

## Installation Notes

- Connect to wifi: `Network Name`
  - Open Network Preferences and add a new location: `Network Location`

### Disk Utility

- Name: `DSTD-MBP13-E2015-DS`
  - **DSTD**: dsthedev
  - **MBP**: MacBook Pro
  - **13**: Screen size
  - **E2015**: Early 2015
  - **DS**: Darren Sopiarz
- Format: `APFS`
- Scheme: `GUID Partition Map`

### New User Info

- Full Name
- Account name will auto populate based on name, don't change
  - Perhaps there should be a naming convention for this?
- Password: Use dsthedev's system based on User Name and year
  - Symbols: `#@`
    - Example: `Damaged#System@19`
  - Hint: Put words used here, no symbols or numbers though

### Non-Express Setup

- Location: `true`
- Analytics: `true` (both)
- Siri: `false`
- Theme: `Dark`

---

## First Steps

It's important to follow these first steps before doing anything else on the computer.  It sets a bunch of sensible defaults and gets Safari setup for safe and efficient browsing.

### General

- Connect to any local network server storage
  - Open Finder and press `cmd+k` or use the Menu item `Go > Connect to Server`
- Download and install the [FiraCode](https://github.com/tonsky/FiraCode) font

### Configuration

#### Dock

Set dock to static mode (only show used apps) `defaults write com.apple.dock static-only -bool true; killall Dock`

 1. Remove *everything* from the docks
 2. Edit dock preferences:
    1. Size: `smallest`
    2. Magnification: `false`
    3. Position on screen: `left`
    4. Minimize windows using: `Scale effect`
    5. Prefer tabs when opening documents: `Always`
    6. Double-click a window's title bar to: `zoom`
    7. Minimize windows into application icon: `true`
    8. Animate opening applications: `false`
    9. Automatically hide and show the Dock: `true`
    10. Show indicators for open applications: `true`
    11. Show recent applications in Dock: `false`

#### Desktop

1. "Show View Options"
   1. Stack By: `None`
   2. Sort By: `Name`
   3. Icon size: `16x16`
   4. Grid spacing: `smallest`
   5. Text size: `10`
   6. Label Position: `Right`
   7. Show item info: `false`
   8. Show icon preview: `false`
2. System Preferences > Desktop & Screen Saver
   1. Desktop:
      1. Use Dynamic Mojave desktop
   2. Screen Saver:
      1. Start after: `20 Minutes`
      2. Show with clock: `true`
      3. Use random screen saver: `false`
      4. Options (Message): `We make the web simple`

#### Finder

1. General:
   1. Show these items on the desktop: `None`
   2. New Finder windows show: `home`
   3. Open folders in tabs instead of new windows: `false`
2. Tags: leave as-is
3. Sidebar: Show these items in the sidebar:
   1. Favorites
      1. Applications
      2. Documents
      3. Downloads
      4. Home (User)
   2. Locations
      1. Hard disks
      2. External disks
      3. Bonjour computers
      4. Connected Servers
4. Advanced
   1. Show all filename extensions: `true`
   2. Show warning before changing an extension: `false`
   3. Show warning before removing from iCloud Drive: `true`
   4. Show warning before emptying the Trash: `false`
   5. Remove items from the Trash after 30 days: `true`
   6. Keep folders on top:
      1. In windows when sorting by name: `true`
      2. On Desktop: `false`
   7. When performing a search: `Search the Current Folder`

#### Menu Bar

1. Battery:
   1. Show Percentage: `true`
2. Date & Time Preferences:
   1. Show date and time in menu bar: `true`
   2. Time options: `Digital`
   3. Display the time with seconds: `true`
   4. Flash the time separators: `false`
   5. Use a 24-hour clock: `true`
   6. Show AM/PM: `disabled`
   7. Date options:
      1. Show the day of the week: `true`
      2. Show date: `true`
   8. Announce the time: `false`

#### Notification Center

1. Today:
   1. Weather: Allow location for automatic

### Accounts & Sync

- iCloud: Use `{name}@dsthedev.com` for Apple ID email
  - General:
    - Upload a professional headshot picture
    - Full First & Last name
    - Contact:
      - Add a personal phone number
      - Add / verify birthday
      - Uncheck all subscriptions
    - Security: Verify Two-Factor Auth is enable with correct phone number
    - Devices: Verify only trusted devices are showing here
    - Payment: N/A
  - Don't sync: Mail, Siri, Stocks, Home
- Time Machine
  - See notes: we should consider implementing a 3-2-1 backup system (hdd/local/cloud)
- Notes App:
  - Preferences:
    - Sort notes by: `Date Created`
    - New notes start with: `Title`
    - Enable the On My Mac account: `false`
    - Default text size: `2`
    - Use dark backgrounds for note content: `true`
    - Locked notes: Set a short easy password for personal notes.
- News:
  - Preferences:
    - Find content in other apps: `true`
    - Restrict stories in Today: `true`
    - Restrict stories with explicit content: `false`
  - Channels & Topics:
    - Remove all defaults
    - Only add relevant channels such as `PHP, SQL, Visual Studio Code, etc`
- Safari:
  - General:
    - Safari opens with: `A new window`
    - New windows open with: `Empty Page`
    - New tabs open with: `Empty Page`
    - Homepage: `about:blank`
    - Remove history items: `After one week`
    - Favorites shows: `Favorites`
    - Top Sites shows: `6 sites`
    - File download location: `Ask for each download`
    - Remove download list items: `Manually`
    - Open "safe" files after downloading: `false`
  - Tabs:
    - Open pages in tabs instead of windows: `Automatically`
    - `cmd+click` opens a link in new tab: `true`
    - When a new window opens, make it active: `false`
    - Use `cmd+(1-9)` to switch tabs: `true`
    - Show website icons in tabs: `true`
  - AutoFill / Passwords:
    - Don't Autofill anything!  Set all to `false`
  - Search:
    - Search engine: `Google`
    - Include search engine suggestions: `false`
    - Include Safari Suggestions: false`
    - Enable Quick Website Search: `false`
    - Preload Top Hit in the background
    - Show Favorites: `true`
  - Security:
    - Warn when visiting a fraudulent website: `true`
    - Enable JavaScript: `true`
  - Privacy:
    - Prevent cross-site tracking: `true`
    - Block all cookies: `false`
  - Websites:
    - @todo: Explore these features to further improve browsing experience
  - Extensions:
    - @todo: Record which extensions are necessary, useful, or should be avoided
  - Advanced:
    - Show full website address: `true`
    - Never use font sizes smaller than: `9`
    - Press Tab to highlight each item on a page: `true`
    - Save articles for offline reading automatically: `false`
    - Stop plug-ins to save power: `true`
    - Style sheet: I recommend `normalize.css` [link](https://necolas.github.io/normalize.css/)
    - Default encoding: `UTF-8`
    - Proxies?  Needs further review
    - Show develop menu in menu bar: `true`

---

## System Preferences

### General

- Appearance: `Dark`
- Accent color: `Green
- Highlight color: `Green`
- Sidebar icon size: `Small`
- Automatically hide and show menu bar: `false`
- Show scroll bars: `Always`
- Click in the scroll bar to: `Jump to the spot thats clicked`
- Default web browsers: `Safari`
- Ask to keep changes when closing documents: `false`
- Close windows when quitting an app: `true`
- Recent items: `None`
- Allow Handoff between this Mac and your iCloud devices: `false`
- Use LCD font smoothing when available: `true`

### Desktop & Screensaver

- This should already be set, see [First Steps > Configuration > Desktop](#First-Steps)

### Dock

- This should already be set, see [First Steps > Configuration > Dock](#First-Steps)

### Mission Control

- Automatically rearrange Spaces based on most recent use: `false`
- When switching to an application, switch to a Space with open windows for the application: `true`
- Group windows by application: `true`
- Displays have separate Spaces: `true`
- Dashboard: `Off`
- Keyboard and Mouse Shortcuts: Leave Defaults

#### Hot Corners

- Bottom Right: `Put Display to Sleep`

### Language & Region

- Only customize this if necessary for a second / different language

### Security & Privacy

#### General

- Require password: `15 minutes` after sleep or screensaver begins
- Show a message when the screen is locked such as `We make the web simple`
- Disable automatic login: `true`
- Allow apps downloaded from: `App Store and identified developers`

#### FileVault

- Only turn on if instructed to, the risk if the key/pass is lost is too much, plus encrypted drives are slower

#### Firewall

- Firewall: `Off`

#### Privacy

- Advertising:
  - Limit Ad Tracking: `true`

### Spotlight

- Search Results:
  - Disable: `Bookmarks & History, Calculator, Mail & Messages, and Spotlight Suggestions`
- Allow Spotlight Suggestions in Look up: `false`
- Privacy: @todo: add any private / personal folders here.

### Notifications

- Do Not Disturb:
  - Turn on Do Not Disturb:
    - From: `9:00 PM` to: `6:00 AM`
    - When the display is sleeping: `false`
    - When mirroring to TV's and projectors: `true`
    - When Do Not Disturb is turned on: All `false`
- Mail: Change alert style to `Alerts`
- Notification Center sort order: `Recents by App`
  - Also, App Store should be synced now, so you can add the following widgets:
    - Battery Monitor
    - Quick Calendar

### Displays

- Show mirroring options in the menu bar when available: `true`
- Display:
  - Resolution: `Scaled (More Space)`
  - Automatically adjust brightness: `false`
- Color:
  - Display Profile: `Color LCD` @todo: Find a way to calibrate and make a custom profile
- Night Shift:
  - Schedule: `Custom`
  - From: `8:00 PM` to `8:00 AM`
  - Manual: Use if necessary
  - Color Temperature: `50%`

### Energy Saver

- Battery:
  - Turn display off after: `10 min`
  - Put hard disks to sleep when possible: `false`
  - Enable Power Nap while on battery power: `false`

---

## General Apps

Apps with an asterisk \* are available on the App Store

- Mail (Apple)
- [Slack](https://slack.com) \*

## Developer Apps

- [Visual Studio Code](https://code.visualstudio.com)
- [Sequel Pro](https://sequelpro.com/test-builds) - Currently using test build (97c1b85783)
  - [SQLPro Studio](https://www.sqlprostudio.com) \* - Maybe try using this instead of Sequel Pro?
- [MAMP](https://www.mamp.info/)
- [Firefox Developer Edition](https://www.mozilla.org/en-US/firefox/developer/)

### Optional Dev Apps

- [BalenaEtcher](https://www.balena.io/etcher/)
- [Hex](https://ridiculousfish.com/hexfiend/)
- [numi](https://numi.io)
- [SiteSucker](https://ricks-apps.com/osx/sitesucker/) \*

---

## Tips & Tricks

- `cmd+shift+.` == Toggle show hidden files / folders
- `option+up/down` == Page up / down
- `cmd+up/down` == Hhome / end
- When using words not recognized by the dictionary, highlight them and select `Learn Spelling` to add them.

## TODO

- Read [this](https://pawelgrzybek.com/change-macos-user-preferences-via-command-line/) and experiment using the command line to change settings instead of the GUI
- Get and document developer Apple ID
- Start using tags and create a useful "system" to follow