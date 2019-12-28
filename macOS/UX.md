# My macOS UX Environment

This post covers how I setup my macOS environment for an optimal user experience. I typically use it for fresh installs, but I also use it as a guide for updating existing machines.

**Warning**: It's kind of a long post!

**Note**: This content is occasionally pulled directly from my [documentation](https://github.com/dsthedev/documentation) repository on GitHub.

**Info**: Items that are crossed out were from Mojave (10.14) that appear to have been removed in Catalina (10.15)

```text
Using macOS Catalina - Version 10.15.2, on a 2015 MacBook Pro.
```

This is a personal guide, follow at your own discretion. If you do, please backup everything you need and remember that I'm not responsible for _your actions_!

## System Preferences

### iCloud

Review Account Details and Features. Personally I provide only the basic account details and turn off all features. I don't care to use iCloud for anything.

### General

| Option                                                 | Value                            |
| ------------------------------------------------------ | -------------------------------- |
| Appearance                                             | `Dark`                           |
| Accent color                                           | `Green`                          |
| Sidebar icon size                                      | `Small`                          |
| Automatically hide and show menu bar                   | `false`                          |
| Show scroll bars                                       | `When Scrolling`                 |
| Click in the scroll bar to                             | `Jump to the spot thats clicked` |
| Default web browsers                                   | `Safari`                         |
| Ask to keep changes when closing documents             | `false`                          |
| Close windows when quitting an app                     | `true`                           |
| Recent items                                           | `None`                           |
| Allow Handoff between this Mac and your iCloud devices | `false`                          |
| Use font smoothing when available                      | `true`                           |

### Desktop & Screen Saver

#### Desktop

Use Catilna's new*er* Dynamic wallpaper because it is awesom*er*.

#### Screensaver

| **Option**              | **Value**                            |
| ----------------------- | ------------------------------------ |
| Screen Saver            | `Message`                            |
| Start after             | `5m`                                 |
| Show with clock         | `true`                               |
| Use random screen saver | `false`                              |
| Screen Saver Options... | Message: `gtfoh`                     |
| Hot Corners...          | Bottom Right: `Put display to sleep` |

For an extremely awesome screen saver check out [Aerial](https://github.com/JohnCoates/Aerial). Be warned though, it can take up _a lot_ of unnecessary resources and bandwidth.

### Dock

First, set the Dock to static mode (only show open apps) with: `defaults write com.apple.dock static-only -bool true; killall Dock`.

| **Option**                             | **Value**             |
| -------------------------------------- | --------------------- |
| Size                                   | `Smallest`            |
| Magnification                          | `false`               |
| Position on Screen                     | `Left`                |
| Minimize windows using                 | `Genie effect`        |
| Prefer tabs when opening documents     | `In Full Screen Only` |
| Double-click a window's title bar to   | `zoom`                |
| Minimize windows into application icon | `true`                |
| Animate opening applications           | `true`                |
| Automatically hide and show the Dock   | `true`                |
| Show indicators for open applications  | `true`                |
| Show recent applications in Dock       | `false`               |

### Mission Control

| **Option**                                                                                | **Value**     |
| ----------------------------------------------------------------------------------------- | ------------- |
| Automatically rearrange Spaces based on most recent use                                   | `false`       |
| When switching to an application, switch to a Space with open windows for the application | `true`        |
| Group windows by application                                                              | `true`        |
| Displays have separate spaces                                                             | `true`        |
| Dashboard \*                                                                              | `Off`         |
| Keyboard and Mouse Shortcuts                                                              | `Disable all` |

\* It appears the Dashboard was removed in Catalina.

### Siri

Disabled

### Spotlight

Disable almost everything from search results except for sensible, static, public, common sources such as Applications, Calculator, Definition, etc.

**Disable** "Allow Spotlight Suggestions in Look up".

### Language & Region

These settings should already be set after the initial installation of macOS. Review for correct settings and customize the advanced date / time settings if desired.

### Notifications

| **Option**                             | **Value**           |
| -------------------------------------- | ------------------- |
| **Turn on Do Not Disturb**             | ...                 |
| From                                   | `10:00pm to 7:00am` |
| When the display is sleeping           | `true`              |
| When the screen is locked              | `true`              |
| When mirroring to TVs and projectors   | `true`              |
| **When Do Not Disturbed is turned on** | ...                 |
| Allow calls from everyone              | `false`             |
| Allow repeated calls                   | `false`             |
| Notification Center sort order         | `Recents`           |
| App alert styles                       | `default`           |

### Internet Accounts

If you've gone through setting up Mail, this section should just be review. Otherwise this is where you'll add accounts that integrate with Mail, Contacts, Notes, and more. Add accounts and configure them appropriately. Also make sure that iCloud is disabled here.

And if there's a Game Center account, disable the Allow Nearby Multiplayer option under Details...

### Users & Groups

This section is mostly only used by administrators, however, I do recommend adding Mail to the Login Items tab and select "Hide".

### Accessibility

| **Option**                            | **Value** |
| ------------------------------------- | --------- |
| Show Accessibility status in menu bar | `false`   |

#### General

~~Disable all~~ Section removed in Catalina.

#### VoiceOver

Disabled

#### Zoom

| Option                                                                         | Value                       |
| ------------------------------------------------------------------------------ | --------------------------- |
| Use keyboard shortcuts to zoom                                                 | `false`                     |
| Use scroll gesture with modifier keys to zoom                                  | `true` - `ctrl+option`      |
| Zoom Style                                                                     | `Picture-in-picture`        |
| Enable Hover Text                                                              | `false`                     |
| **Advanced (Appearance)**                                                      | ...                         |
| When zoomed in, the screen image moves:                                        | `Continuously with pointer` |
| Invert colors                                                                  | `false`                     |
| Smooth images                                                                  | `true`                      |
| Flash screen when notification banner appears outside zoom view                | `false`                     |
| Follow keyboard focus                                                          | `false`                     |
| Keep zoom window stationary                                                    | `false`                     |
| Adjust Size and Location                                                       | _Yes_                       |
| ~~Speak items under the pointer~~                                              | `false`                     |
| **Advanced (Controls)**                                                        | ...                         |
| Hold `ctrl+option` to temporarily toggle zoom                                  | `true`                      |
| Hold `ctrl+cmd` to temporarily detach zoom view from pointer                   | `false`                     |
| Press `option+cmd+F` to toggle between full screen and picture-in-picture zoom | `false`                     |
| Use keyboard shortcuts to adjust zoom window (`ctrl+option+cmd+arrowkeys`)     | `true`                      |
| Use trackpad gesture to zoom (Double-tap three fingers / drag)                 | `true`                      |
| **Options**                                                                    |                             |
| ~~Window position~~                                                            | `Follow mouse cursor`       |
| ~~Cursor style~~                                                               | `System cursor`             |

The hover text option looks really nice, but I'm not really sure how practical it is; needs real world testing.

#### Display

| Option                        | Value    |
| ----------------------------- | -------- |
| Invert colors                 | `false`  |
| Reduce motion                 | `false`  |
| Increase contrast             | `false`  |
| Reduce transparency           | `true`   |
| Differentiate without color   | `false`  |
| ~~Use grayscale~~             | `false`  |
| Display contrast              | `Normal` |
| Shake mouse pointer to locate | `true`   |
| Cursor size                   | `Normal` |
| Enable Color Filters          | `false`  |

#### Speech

| Option                                      | Value      |
| ------------------------------------------- | ---------- |
| System Voice                                | `Samantha` |
| Speaking Rate                               | `Normal`   |
| Enable announcements                        | `false`    |
| Speak selected text when the key is pressed | `false`    |
| Speak items under the pointer               | `false`    |

#### Descriptions

| **Option**                             | **Value** |
| -------------------------------------- | --------- |
| Play audio descriptions when available | `false`   |

#### Audio

| **Option**                                  | **Value** |
| ------------------------------------------- | --------- |
| Flash the screen when an alert sound occurs | `false`   |
| Play stereo audio as mono                   | `false`   |

#### Captions

| **Option**                     | **Value**              |
| ------------------------------ | ---------------------- |
| Style                          | Transparent Background |
| Prefer closed captions and SDH | `false`                |

#### Voice Control

Disable all.

#### Keyboard

| **Option**         | **Value** |
| ------------------ | --------- |
| Enable Sticky Keys | `false`   |
| Enable Slow Keys   | `false`   |

"Keyboard Preferences..." should've already been set earlier. If not, use the button to review or update them.

#### ~~Dictation~~

~~All options are disabled and grayed out.~~

#### Pointer Control

| **Option**                                                          | **Value** |
| ------------------------------------------------------------------- | --------- |
| Double-click speed                                                  | `9/11`    |
| Spring-loading delay                                                | `1/11`    |
| Ignore built-in trackpad when mouse or wireless trackpad is present | `false`   |
| **Alternate Control Methods**                                       | ...       |
| Enable Mouse Keys                                                   | `false`   |
| Enable Alternate Pointer Actions                                    | `false`   |

#### Switch Control

I've never used this and don't think I ever will, all options should be disabled.

#### Siri

| **Option**          | **Value** |
| ------------------- | --------- |
| Enable Type to Siri | `false`   |

#### Shortcut

Disable all except for Zoom

##### ~~Trackpad Options~~

| **Option**          | **Value**                 |
| ------------------- | ------------------------- |
| ~~Scrolling speed~~ | ~~`5/8` ~~                |
| ~~Scrolling ~~      | ~~`true` - with inertia~~ |
| ~~Enable dragging~~ | ~~`false` ~~              |

##### ~~Mouse Options~~

| **Option**          | **Value** |
| ------------------- | --------- |
| ~~Scrolling speed~~ | ~~`5/8`~~ |

### Screen Time

**New feature**, enable basic usage for now just to view app usage and consider using advanced features later.

### Extensions

| **Section**       | **Extensions**                     |
| ----------------- | ---------------------------------- |
| All               | `None`                             |
| Actions           | `Markup`                           |
| Finder Extensions | `None` (Disable iCloud Drive)      |
| Photos Editing    | `None`                             |
| Quick Look        | `None`                             |
| Share Menu        | `Remove all`                       |
| Today             | `Remove all`                       |
| Finder            | `Rotate, Markup, Create PDF, Trim` |

### Security & Privacy

The default settings in this section should be fine, again I recommend going through and making sure nothing looks off.

Except for one thing, under the Privacy tab, find the Advertising feature and enable `Limit Ad Tracking`.

Eventually, the Firewall and Privacy tabs should be reviewed and tweaked, eventually.

### Software Update

Always make sure your Mac is up to date!

| Option                               | Value   |
| ------------------------------------ | ------- |
| Automatically keep my Mac up to date | `false` |

#### Advanced (Automatic Options)

| **Option**                                     | **Value** |
| ---------------------------------------------- | --------- |
| Check for updates                              | `true`    |
| Download new updates when available            | `true`    |
| Install macOS updates                          | `false`   |
| Install app updates from the App Store         | `false`   |
| Install system data files and security updates | `true`    |

### Network

If you connected to Wi-Fi during the initial installation, this section shouldn't need any further changes; the defaults are fine.

| Option                          | Value                  |
| ------------------------------- | ---------------------- |
| Location                        | Setup Common Locations |
| Status                          | `Connected`            |
| Network Name                    | `Desired Network Name` |
| Automatically join this network | `true`                 |
| Ask to join Personal Hotspots   | `false`                |
| Ask to join new networks        | `false`                |
| Show Wi-Fi status in menu bar   | `true`                 |
| **Advanced**                    | ...                    |
| DNS                             | Add `1.1.1.1`          |

**Note**: Typically I setup a static IP for my home location, but this should be handled at the router level, not here; although you can double check it under TCP/IP.

### Bluetooth

| Option                     | Value   |
| -------------------------- | ------- |
| Bluetooth                  | `Off`   |
| Show Bluetooth in menu bar | `false` |

Occasionally I will use bluetooth headphones, but instead of having it on all the time, simply enable and add when necessary (long flights or quiet sessions).

### Sound

#### Global

| Option                  | Value        |
| ----------------------- | ------------ |
| Output Volume           | `25% (4/16)` |
| Show volume in menu bar | `false`      |

#### Sound Effects

| Option                               | Value               |
| ------------------------------------ | ------------------- |
| Alert Sound                          | `Morse`             |
| Play sound effects through           | `Internal Speakers` |
| Alert volume                         | `~75%`              |
| Play user interface sound effects    | `true`              |
| Play feedback when volume is changed | `true`              |

#### Output

| Option  | Value               |
| ------- | ------------------- |
| Device  | `Internal Speakers` |
| Balance | `Centered`          |

#### Input

| Option                          | Value                 |
| ------------------------------- | --------------------- |
| Device                          | `Internal Microphone` |
| Input Volume                    | `50%`                 |
| ~~Use ambient noise reduction~~ | ~~`true`~~            |

### Printers & Scanners

I almost never print anything, but if you have a printer, add it here.

| **Option**         | **Value**           |
| ------------------ | ------------------- |
| Default printer    | `Last Printer Used` |
| Default paper size | `US Letter`         |

### Keyboard

#### Keyboard

| Option                                                          | Value   |
| --------------------------------------------------------------- | ------- |
| Key Repeat                                                      | `Fast`  |
| Delay Until Repeat                                              | `Short` |
| Adjust keyboard brightness in low light                         | `false` |
| Turn keyboard backlight off after `[time period]` of inactivity | `false` |
| Show keyboard and emoji viewers in menu bar                     | `false` |
| Use F1, F2, etc. keys as standard function keys                 | `false` |

#### Text

| Option                         | Value                   |
| ------------------------------ | ----------------------- |
| Replace / With List            | ...                     |
| Replace `shrug`                | `¯\_(ツ)_/¯`            |
| Correct spelling automatically | `true`                  |
| Capitalize words automatically | `true`                  |
| Add period with double-space   | `true`                  |
| Spelling                       | `Automatic by Language` |
| Use smart quotes and dashes    | `false`                 |

It looks like they added the shrug text emoji in Catalina?! Nice.

#### Shortcuts

| Option                                                 | Value  |
| ------------------------------------------------------ | ------ |
| Use keyboard navigation to move focus between controls | `true` |

#### Input Sources

| Option                      | Value   |
| --------------------------- | ------- |
| Source                      | `U.S`   |
| Show Input menu in menu bar | `false` |

#### Dictation

| Option    | Value     |
| --------- | --------- |
| Dictation | `Off`     |
| Language  | `English` |
| Shortcut  | `Off`     |

### Trackpad

#### Point & Click

| Option                          | Value                                |
| ------------------------------- | ------------------------------------ |
| Look up & data detectors        | `true` - Force click with one finger |
| Secondary click                 | `true` - Click with two fingers      |
| Tap to click                    | `false`                              |
| Click                           | `Medium`                             |
| Tracking Speed                  | `~55%`                               |
| Silent Clicking                 | `true`                               |
| Force Click and haptic feedback | `true`                               |

#### Scroll & Zoom

| Option                    | Value  |
| ------------------------- | ------ |
| Scroll direction: Natural | `true` |
| Zoom in or out            | `true` |
| Smart zoom                | `true` |
| Rotate                    | `true` |

#### More Gestures

| **Option**                     | **Value**                                              |
| ------------------------------ | ------------------------------------------------------ |
| Swipe between pages            | `true` - Scroll left or right with 2 fingers           |
| Swipe between full-screen apps | `true` - Swipe left or right with 3 fingers            |
| Notification Center            | `true` - Swipe left from the right edge with 2 fingers |
| Mission Control                | `true` - Swipe up with 3 fingers                       |
| App Exposé                     | `false`                                                |
| Launchpad                      | `false`                                                |
| Show Desktop                   | `false`                                                |

### Mouse

I don't use a mouse with my MacBook Pro, but if you do then connect it here and configure it.

### Displays

| Option                                                | Value  |
| ----------------------------------------------------- | ------ |
| Airplay Display                                       | `Off`  |
| Show mirroring options in the menu bar when available | `true` |

#### Display

| Option     | Value                 |
| ---------- | --------------------- |
| Resolution | `Scaled > More Space` |
| Brightness | `50% / Auto`          |

#### Color

| Option          | Value       |
| --------------- | ----------- |
| Display Profile | `Color LCD` |

#### Nightshift

| Option            | Value              |
| ----------------- | ------------------ |
| Schedule          | `Custom`           |
| From              | `8:00pm to 8:00am` |
| Color Temperature | `~55% (default)`   |

### Energy Saver

#### Battery

| Option                                          | Value   |
| ----------------------------------------------- | ------- |
| Turn display off after                          | `5m`    |
| Put hard disks to sleep when possible           | `false` |
| Slightly dim the display while on battery power | `true`  |
| Enable Power Nap while on battery power         | `false` |

#### Power Adapter

| Option                                                               | Value   |
| -------------------------------------------------------------------- | ------- |
| Turn display off after                                               | `10m`   |
| Prevent computer from sleeping automatically when the display is off | `false` |
| Put hard disks to sleep when possible                                | `false` |
| Wake for network access                                              | `true`  |
| Enable Power Nap while plugged into a power adapter                  | `true`  |

### Date & Time

#### Date & Time

Double check everything is right.

#### Timezone

Double check everything is right.

#### Clock

| Option                         | Value     |
| ------------------------------ | --------- |
| Show date and time in menu bar | `true`    |
| **Time options**               | `Digital` |
| Display the time with seconds  | `true`    |
| Flash the time separators      | `false`   |
| Use a 24-hour clock            | `true`    |
| Show AM/PM                     | `false`   |
| **Date Options**               |           |
| Show the day of the week       | `true`    |
| Show date                      | `true`    |
| Announce the time              | `false`   |

### Sharing

As of right now, this is my only Apple device so all sharing options are disabled.

### Parental Controls

I don't use these, and it's for administrators only anyways.

**Note**: This only shows up with at least 2 accounts.

### Time Machine

Disabled

### Startup Disk

This section displays which disk is being used for startup and what version of macOS is on it. There aren't any options here, however, take note of the "Target Disk Mode..." button; it allows booting without needing to hold `option` to access the boot selector mode.

---

## Extra Tweaks

### Finder

First, open the root directory, right click, select Show View Options, and do this:

| Option                     | Value  |
| -------------------------- | ------ |
| Always open in column view | `true` |
| Browse in column view      | `true` |
| Group by                   | `Kind` |
| Sort by                    | `Name` |
| Text size                  | `12`   |
| Show icons                 | `true` |
| Show icon preview          | `true` |
| Show preview column        | `true` |

This should apply these rules to all other finder windows when opened, hopefully.

Use `cmd+,` to open the rest of these settings for Finder.

#### General

| Option                                      | Value                   |
| ------------------------------------------- | ----------------------- |
| Show these items on the desktop             | `false` for all options |
| New Finder windows show                     | `{userhomefolder}`      |
| Open folders in tabs instead of new windows | `false`                 |

#### Tags

| Option                         | Value                                        |
| ------------------------------ | -------------------------------------------- |
| Show these tags in the sidebar | `Uncheck All`                                |
| Favorite Tags                  | Remove all tags except for one as a reminder |

#### Sidebar

| Option                          | Value  |
| ------------------------------- | ------ |
| Show these items in the sidebar | ...    |
| Applications                    | `true` |
| `{userhomefolder}`              | `true` |
| Hard Disks                      | `true` |
| External Disks                  | `true` |
| Bonjour computers               | `true` |
| Connected servers               | `true` |
| Tags                            | `none` |

#### Advanced

| Option                                         | Value                       |
| ---------------------------------------------- | --------------------------- |
| Show all filename extensions                   | `true`                      |
| Show warning before changing an extension      | `true`                      |
| Show warning before removing from iCloud Drive | `true`                      |
| Show warning before emptying the Trash         | `true`                      |
| Remove items from the Trash after 30 days      | `true`                      |
| Keep folders on top                            | ...                         |
| In windows when sorting by name                | `true`                      |
| On Desktop                                     | `true`                      |
| When performing a search                       | `Search the Current Folder` |

## Conclusion

If you're reading this you're either me, or are surprisingly invested in how I setup my macOS environment.  Either way, this is basically just the beginning of how I customize my macOS system.  I also have documentation for how I setup Safari & Mail as well.  I plan on adding more to this series soon, including homebrew and hopefully a script to automate a bunch of this.

Thanks for reading, enjoy your awesome new macOS environment!
