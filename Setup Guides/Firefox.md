# Setting up Firefox

Before changing anything, remember the purpose of using both Firefox and Firefox Developer Edition:

- Firefox (Regular) is only for viewing PDF's, so most settings don't really matter other than the default download location (meh).
- Firefox Developer Edition is my main browser for web development, so keep the following in mind:
   - Any site functionality that is expected of regular users should be kept (font size, location, etc)

1. Customize - Remove everything except for Developer, Home, and Fullscreen
2. Preferences
   1. General
      1. General
         1. Startup
            1. Allow Firefox Developer Edition and Firefox to run at the same time: `true`
            2. Restore previous session: `false`
            3. Always check if FF is your default browser: `false`
         2. Tabs
            1. `Ctrl + Tab` cycles through recent tabs: `false`
            2. Open links in tabs instead of windows: `true`
            3. When you open a link in a new tab, switch to it immediately: `false`
            4. Show tab previews in the Windows taskbar: `true`
         3. Home
            1. New Windows and Tabs
               1. Homepage and new windows: `https://db.d11z.me/`
               2. New Tabs: `Blank Page`
      2. Language and Appearance
          1. Fonts & Colors
             1. Leave all font settings at defaults!
          2. Language
             1. Check your spelling as you type: `true`
      3. Files and Applications
          1. Downloads
             1. Always ask you where to save files
   2. Privacy & Security

- Custom settings:
- Uncheck remember browsing/download history
- Uncheck remember search/form history
- Clear history when FFDE closes
- Location Bar - Only check bookmarks for suggestions
- Tracking protection set to always
- Send "Do Not Track" signal to sites, always
- Security - Don't remember logins for sites