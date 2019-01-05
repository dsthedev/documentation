# Documentation Changes

Safari
MacOS (Mojave)
Terminal
VSCode

---

## MacOS (Mojave)

This is going to need a complete overhaul most likely as Apple has moved to Mojave from High Sierra.

### General Order

- Safari
- Homebrew
- VSCode

### Shortcuts

- `cmd+shift+.`: Temporarily show hidden stuff in Finder

### Mac Apps

#### Safari

- Add screenshots in `~/Desktop/DocShots`

##### General

- Safari opens with: `A new private window`
- New windows open with: `Homepage`
  - `https://db.d11z.me`
- New tabs open with: `Empty Page`
- Homepage: `about:blank`
- Remove history items: `After one day`
- Favorites shows: `Favorites`
- Top Sites shows: `6 sites`
- File download location: `Ask for each download`
- Remove download list items: `Manually`
- Open "safe" files after downloading: `false`

##### Tabs

- Open pages in tabs instead of windows: `Automatically`
- `cmd+click` opens a link in new tab: `true`
- When a new window opens, make it active: `false`
- Use `cmd+(1-9)` to switch tabs: `true`
- Show website icons in tabs: `true`

##### AutoFill / Passwords

- Don't Autofill anything!  Set all to `false`

##### Search

- Search engine: `Google`
- Uncheck everything except for favorites in the Smart Search Field.

##### Security

- Check all (warn of fraudulent sites, enable JS, block pop-ups)

##### Privacy

- Prevent cross-site tracking: `true`
- Ask websites not to track me: `true`
- Block all cookies: `false`

##### Websites

- Reader: Set "When visiting other websites" to `On`
	- This will automatically add new sites to the auto-reader list
- No need to enable dark mode if using macOS in dark mode

##### Extensions

- Needs further review

##### Advanced

- Show full website address: `true`
- Never use font sizes smaller than: `9`
- Press Tab to highlight each item on a page: `false`
- Save articles for offline reading automatically: `true`
- Stop plug-ins to save power: `true`
- Style sheet: I recommend `normalize.css` [link](https://necolas.github.io/normalize.css/)
- Default encoding: `UTF-8`
- Proxies?  Needs further review
- Show develop menu in menu bar: `true`

##### Bookmarks

- Remove ALL
  - Add as needed / used

---

## Non "Mac" Apps

---

### Synergy

- **Note:**  The transfer edge needs to align with the monitor arrangement in macOS.

### MAMP

- Add screenshots in `~/Desktop/DocShots`

- Download & Install (No Pro)
- Setup
    - Start/Stop
        - Start servers: `true`
        - Check for MAMP PRO: `false`
        - Open WebStart page: `false`
        - When quitting MAMP, Stop servers: `true`
    - Ports: `Set Web & MySQL ports to 80 & 3306`
    - PHP: Latest and no cache
    - Web Server: Apache & Default Document Root

### VSCode

- Show welcome screen on startup: `newUntitledFile`

#### Extensions

- Markdown All in One

### Display Menu

- Display Menu, mostly for external monitors