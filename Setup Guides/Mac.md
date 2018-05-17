# Mac Setup

This is for after a clean install of the latest version of macOS (Currently High Sierra)

---

## First Steps

- Upgrade to macOS HighSierra if not already installed
- Update all apps if available

---

## System Preferences

- u

## Applications

- Synergy

---

## CLI's

- Homebrew
- Node@8
- nvm?

---

### App Setup (Manual)

#### Finder

##### General

- Show these items on the desktop: `none`
- New Finder windows show: `{User's Home}`
- Open folders in tabs instead of new windows: `false`

##### Tags

**@todo** Start using tags, and create a useful "system" to follow.

##### Sidebar

- Show these items in the sidebar:
	- Favorites: `{User's Home}`
	- Shared: `Connected servers`
	- Devices: `{User's Home} {Mac type}, External disks`
	- Tags: `none`

##### Advanced

- Show all filename extensions: `true`
- Show warning before changing an extension: `false`
- Show warning before removing from iCloud Drive: `true`
- Show warning before emptying the Trash: `false`
- Remove items from the Trash after 30 days: `true`
- Keep folders on top when sorting by name: `true`
- When performing a search: `Search the Current Folder`

#### Safari

##### General

- Safari opens with: `A new window`
- New windows open with: `Empty Page`
- New tabs open with: `Empty Page`
- Homepage: `about:blank`
- Remove history items: `After one day`
- Favorites shows: `Favorites`
- Top Sites shows: `6 sites`
- File download location: `Ask for each download`
- Remove download list items: `Manually`
- Open "safe" files after downloading: `false`

---

## Automated

Because macOS is awesome, system prefernces and most programs can be installed and configured via the terminal.

### App Setup (Terminal)

#### Finder

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

#### Safari

- Open "safe" files after downloading: `defaults write com.apple.Safari AutoOpenSafeDownloads -bool false`

#### System Preferences

- Disable natural scrolling (trackpad only): `defaults write NSGlobalDomain com.apple.swipescrolldirection -bool false`

#### Dock

- Remove all default icons from the Dock:
	- `defaults delete com.apple.dock persistent-apps`
	- `defaults delete com.apple.dock persistent-others`
	- `killall Dock`
- Add a spacer to the Dock:
	- `defaults write com.apple.dock persistent-apps -array-add '{"tile-type"="spacer-tile";}'`
	- `killall Dock`

#### General

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
- Guides
	- [The Ultimate Must-Know Guide to Securely Deleting Private Files & Folders from Your Mac Forever](https://mac-how-to.gadgethacks.com/how-to/ultimate-must-know-guide-securely-deleting-private-files-folders-from-your-mac-forever-0145979/)
