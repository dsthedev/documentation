# Mac Setup

This is for after a clean install of the latest version of macOS (Currently High Sierra)

**Note:** For now, I'm sticking with the MacOS extended file format instead of APFS.

---

## First Steps

After installing a fresh copy of macOS with a master admin account (Commander), follow the options below before creating a standard user account.

- Upgrade to macOS HighSierra if not already installed
- Update all apps if available
- Complete Keyboard Setup Assistant if needed
- If Auto Update Popup shows select "Not Now", it will still notify when updates are available
- Setup Safari per instructions below
- *Optional*: Download, install, and configure Synergy

Now that some sensible defaults have been set for the admin account (should rarely be used), it's time to create a Standard user account and get it setup with some similarly sensible defaults too.  It may seem redundant, but if this is a personal device it's nice to have a familiar environment if you ever have to switch accounts.

- Create the Standard User account in `System Preferences > Users & Groups`

---

## System Preferences

### General

- Appearance: `Graphite`
- Use dark menu bar and Dock: `true`
- Automatically hide and show menu bar: `false`

### Users & Groups

- Login Options:
	- Display login window as: `Name and password`
	- Show the Sleep, Restart, and Shutdown buttons: `false`
	- Show fast user switching menu as `Account Name`
	- Basically all options are set to `false/off`

---

## Applications to Install

### Required Apps

- Synergy

### Recommended Apps

- Slack

---

## CLI's

- Homebrew
- Node@8
- nvm?

---

## App Setup (Manual)

If you'd rather setup applications via the terminal, skip to the next section.

### Finder

#### General

- Show these items on the desktop: `none`
- New Finder windows show: `{User's Home}`
- Open folders in tabs instead of new windows: `false`

#### Tags

**@todo** Start using tags, and create a useful "system" to follow.

#### Sidebar

- Show these items in the sidebar:
	- Favorites: `{User's Home}`
	- Shared: `Connected servers`
	- Devices: `{User's Home} {Mac type}, External disks`
	- Tags: `none`

#### Advanced

- Show all filename extensions: `true`
- Show warning before changing an extension: `false`
- Show warning before removing from iCloud Drive: `true`
- Show warning before emptying the Trash: `false`
- Remove items from the Trash after 30 days: `true`
- Keep folders on top when sorting by name: `true`
- When performing a search: `Search the Current Folder`

### Safari

For regular usage, especially on a Mac, Safari is actually a really good browser.  The fact that it's not cross platform (obviously) is a bummer, but it has some nice features that make browsing the web slightly more pleasant than other browsers.  Plus performance and OS integration are top notch.

#### General

- Safari opens with: `A new private window`
- New windows open with: `Empty Page`
- New tabs open with: `Empty Page`
- Homepage: `about:blank`
- Remove history items: `After one day`
- Favorites shows: `Favorites`
- Top Sites shows: `6 sites`
- File download location: `Ask for each download`
- Remove download list items: `Manually`
- Open "safe" files after downloading: `false`

#### Tabs

- Open pages in tabs instead of windows: `Automatically`
- `cmd+click` opens a link in new tab: `true`
- When a new window opens, make it active: `false`
- Use `cmd+(1-9)` to switch tabs: `true`

#### AutoFill / Passwords

- Don't Autofill anything!  Set all to `false`

#### Search

- Search engine: `Google`
	- I'm considering using DuckDuckGo, just haven't found time
- Uncheck everything except for favorites in the Smart Search Field.

#### Security

- Check all (warn of fraudulent sites, enable JS, block pop-ups)

#### Privacy

- Prevent cross-site tracking: `true`
- Ask websites not to track me: `true`
- Block all cookies: `false`

#### Websites

This appears to be a very useful section to fine tune my browsing experience.

- Reader: Set "When visiting other websites" to `On`
	- This will automatically add new sites to the auto-reader list
	- Also make the reader dark by opening an article with reader enabled to access the reader settings for color and font type

#### Extensions

Needs further review:

- Grammarly
- URL Advisor by Kaspersky

#### Advanced

- Show full website address: `true`
- Never use font sizes smaller than: `9`
- Press Tab to highlight each item on a page: `true`
- Save articles for offline reading automatically: `true`
- Stop plug-ins to save power: `true`
- Style sheet: I recommend `normalize.css` [link](https://necolas.github.io/normalize.css/)
- Default encoding: `UTF-8`
- Proxies?  Needs further review
- Show develop menu in menu bar: `true`

---

## App Setup (Terminal)

Because macOS is awesome, system prefernces and most programs can be installed and configured via the terminal.

### Finder

- Always show scroll bars: `defaults write NSGlobalDomain AppleShowScrollBars -string "Always"`
- Expand save & print panels by default:
	- `defaults write NSGlobalDomain NSNavPanelExpandedStateForSaveMode -bool true`
	- `defaults write NSGlobalDomain NSNavPanelExpandedStateForSaveMode2 -bool true`
	- `defaults write NSGlobalDomain PMPrintingExpandedStateForPrint -bool true`
	- `defaults write NSGlobalDomain PMPrintingExpandedStateForPrint2 -bool true`
- Show hidden files & folders:
	- `defaults write com.apple.finder AppleShowAllFiles -bool true`
	- `killall Finder`
	- Individually:
		- `chflags nohidden ~/Library/`
		- `chflags hidden ~/Documents/Secrets`
- Open finder window when a drive is mounted:
	- `defaults write com.apple.frameworks.diskimages auto-open-ro-root -bool true`
	- `defaults write com.apple.frameworks.diskimages auto-open-rw-root -bool true`
	- `defaults write com.apple.finder OpenWindowForNewRemovableDisk -bool true`
- Disable warning before emptying the Trash: `defaults write com.apple.finder WarnOnEmptyTrash -bool false`

### Safari

- Open "safe" files after downloading: `defaults write com.apple.Safari AutoOpenSafeDownloads -bool false`

### System Preferences

- Disable natural scrolling (trackpad only): `defaults write NSGlobalDomain com.apple.swipescrolldirection -bool false`

### Dock

- Remove all default icons from the Dock:
	- `defaults delete com.apple.dock persistent-apps`
	- `defaults delete com.apple.dock persistent-others`
	- `killall Dock`
- Add a spacer to the Dock:
	- `defaults write com.apple.dock persistent-apps -array-add '{"tile-type"="spacer-tile";}'`
	- `killall Dock`

### General

- Check for software updates daily: `defaults write com.apple.SoftwareUpdate ScheduleFrequency -int 1`
- Change screenshot file type: `defaults write com.apple.screencapture type -string "png"`
- Change screenshot location:
	- `defaults write com.apple.screencapture location /Users/{Username}/Desktop/`
	- `killall SystemUIServer`
- Lower boot up sound volume:
	- `sudo nvram SystemAudioVolume="%50"`
	- Reset: `sudo nvram -d SystemAudioVolume`
- Enable text selection & copy in Quick Look:
	- `defaults write com.apple.finder QLEnableTextSelection -bool TRUE;`
	- `killall Finder`

**@todo** Create a script that updates system preferences, installs applications, and gets as close to a "ready-to-use" state as possible.

---

## Shortcut Reference

- `cmd+,` open current app's preferences

---

## Terminal Reference

- Securely delete a file:
	- File: `srm -s /draggedfile`
	- File (7 passes): `srm -m /draggedfile`
	- Folder: `srm -rf /draggedfolder`
- Find available domains: `defaults domains | tr ',' '\n'`

---

## Resources

- Applications
	- [Synergy](https://symless.com/synergy)
- Terminal
	- [Change macOS user preferences via command line](https://pawelgrzybek.com/change-macos-user-preferences-via-command-line/)
	- [Change OS X’s Annoying Default Settings Using Terminal](https://mac-how-to.gadgethacks.com/how-to/change-os-x-s-annoying-default-settings-using-terminal-0162471/)
	- [13 Terminal Commands Every Mac User Should Know](https://mac-how-to.gadgethacks.com/how-to/13-terminal-commands-every-mac-user-should-know-0162453/)
	- [6 Tweaks You Should Be Using on Your Mac Right Now](https://mac-how-to.gadgethacks.com/how-to/6-tweaks-you-should-be-using-your-mac-right-now-0161605/)
- Bash
	- [Nate Landau's Mac OSX Bash Profile](https://natelandau.com/my-mac-osx-bash_profile/)
- Homebrew
	- [Homebrew Formulae](https://formulae.brew.sh/formula/)
	- [Papo's macosx app setup list using brew and cask](http://javapapo.blogspot.com/2015/08/my-macosx-app-setup-list-using-brew-and.html)
- Guides
	- [The Ultimate Must-Know Guide to Securely Deleting Private Files & Folders from Your Mac Forever](https://mac-how-to.gadgethacks.com/how-to/ultimate-must-know-guide-securely-deleting-private-files-folders-from-your-mac-forever-0145979/)
