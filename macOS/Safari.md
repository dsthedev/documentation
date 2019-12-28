# Safari

This post covers how I setup Safari on my MacBook Pro for personal use. It covers usage, preferences, shortcuts, and some tips.

**Note**: This content is occasionally pulled directly from my [documentation](https://github.com/dsthedev/documentation) repository on GitHub.

**Info**: Items that are crossed out were from Mojave (10.14) that appear to have been removed in Catalina (10.15)

```text
Using macOS Catalina - Version 10.15.2, on a 2015 MacBook Pro.
```

This is a personal guide, follow at your own discretion. If you do, please backup everything you need and remember that I'm not responsible for _your actions_!

## Preferences

To open the preferences panel, simply press `cmd+,` with Safari active or use the Menu Bar Under `Safari > Preferences...`

### General

| Option                              | Value                   |
| ----------------------------------- | ----------------------- |
| Safari opens with                   | `A new private window`  |
| New windows open with               | `Homepage`              |
| New tabs open with                  | `Empty Page`            |
| Homepage                            | `https://db.d11z.me/`   |
| Remove history items                | `After one day`         |
| Favorites shows                     | `Favorites`             |
| Top Sites shows                     | `6 sites`               |
| File download location              | `Ask for each download` |
| Remove download list items          | `Manually`              |
| Open "safe" files after downloading | `false`                 |

### Tabs

| Option                                  | Value           |
| --------------------------------------- | --------------- |
| Open pages in tabs instead of windows   | `Automatically` |
| `cmd+click` opens a link in new tab     | `true`          |
| When a new window opens, make it active | `false`         |
| Use `cmd+(1-9)` to switch tabs          | `true`          |
| Show website icons in tabs              | `true`          |

### AutoFill / Passwords

Don't Autofill anything! Set all to `false`

### Search

| Option                            | Value         |
| --------------------------------- | ------------- |
| Search engine                     | `DuckDuckGo`  |
| Include search engine suggestions | `false`       |
| Smart Search Field                | `Uncheck all` |

### Security

| Option                                  | Value  |
| --------------------------------------- | ------ |
| Warn when visiting a fraudulent website | `true` |
| Enable JavaScript                       | `true` |

### Privacy

| Option                           | Value   |
| -------------------------------- | ------- |
| Prevent cross-site tracking      | `true`  |
| ~~Ask websites not to track me~~ | `true`  |
| Block all cookies                | `false` |

### Websites

| Option                       | Value         |
| ---------------------------- | ------------- |
| When visiting other websites | `Off`         |
| Reader Shortcut              | `cmd+shift+R` |

**Note**: Safari's reader mode is dope, I highly recommend using it on any site where the main purpose is reading large amounts of text.

### Extensions

None

### Advanced

| Option                                          | Value                           |
| ----------------------------------------------- | ------------------------------- |
| Show full website address                       | `true`                          |
| Never use font sizes smaller than               | `9`                             |
| Press Tab to highlight each item on a page      | `false`                         |
| Save articles for offline reading automatically | `false`                         |
| Stop plug-ins to save power                     | `true`                          |
| Style sheet                                     | `~/Resources/CSS/normalize.css` |
| Default encoding                                | `UTF-8`                         |
| Proxies?                                        | Needs further review            |
| Show develop menu in menu bar                   | `true`                          |

## Bookmarks

1. Edit Bookmarks with `cmd+opt+B`
2. Remove all default bookmarks
3. Import from `usb/Resources/Bookmarks/Safari\ Bookmarks.html`
4. Move all from `Imported/Favorites` to `*Favorites`
5. Show bookmark bar with `cmd+shift+B`

## Conclusion

Despite all the hate this browser might get from people, it's hands down the best daily browser on macOS desktops.  Of course it shouldn't be your only browser though, as having different browsers for different uses is just plain smart; for example use Firefox Dev Edition for webdev and Opera Dev for development R&D.