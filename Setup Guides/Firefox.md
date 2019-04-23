# Firefox

First things first, go through the preferences and configure all settings properly to protect and serve the user.

Afterwards, download the Developer Edition and set it up in almost the same way.  Differences will be marked below.  Even if you're not doing web development, the tools for inspecting a website's source code are amazing and useful in general.

If you're using Windows, Firefox is basically the best option as a PDF viewer.  If you're on Linux Mint (Cinnamon) or macOS, their preview apps are better, so there's really no need to download or use the regular Firefox Edition.

## Preferences

### General

#### General

##### Startup

- Restore previous session: `false`
  - _I prefer to have a fresh start every time I open a browser_
- Always check if Firefox is your default browser: `false`
  - _My preferred default browser is Opera_

##### Tabs

- `Ctrl+Tab` cycles through tabs in recently used order: `false`
  - _I prefer a consistent and predictable order_
- Open links in tabs instead of new windows: `true`
  - _It's kind of why we created tabs in the first place, right?_
- When you open a link in a new tab, switch to it immediately: `false`
  - _Most links I click are meant to be read later, not immediately_

#### Language and Appearance

##### Fonts & Colors

- Default font: Keep the default fonts, sizes, colors, etc.
  - _Mostly because not allowing custom fonts can break both functionality and/or design on some sites_
- Choose the languages used to display menus, messages, and notifications from Firefox: `English (United States)`
- Choose your preferred language for displaying pages: `English (United States) [en-us]`
- Check your spelling as you type: `true`
  - _It's a nice visual cue, but not necessary_

#### Files and Applications

##### Downloads

- Always ask you where to save files: `true`
  - _Helps force me to organize files preemptively, rather than trying to clean up the Downloads folder later (a.k.a never)_

##### Applications

- Choose how Firefox handles the files you download from the web or the applications you use while browsing: Keep the default settings here until further review

##### Digital Rights Management (DRM) Content

- Play DRM-controlled content: `false`
  - _From what I can tell, this allows companies to run potentially harmful closed-source binaries on your machine (even if it's in a sandbox environment)_

#### Firefox Updates

- Automatically update search engines: `true`
  - _I can't imagine using an outdated search engine will yield the best results, I could be wrong though

#### Performance

- Use recommended performance settings: `true`
  - _I haven't read up on what these settings really do or ran any tests yet_

#### Browsing

- Use autoscrolling: `false`
  - _Why?_
- Use smooth scrolling: `true`
  - _I'm a fan of smoother experiences_
- Always use the cursor keys to navigate within pages: false
  - _No, I prefer the scroll wheel, and it might interfere with some sites custom functionality_
- Search for text when you start typing: `false`
  - _That's what ctrl+f is for_
- Recommend extensions as you browse: `false`
  - _Meh, this could be useful, but I can't remember the last time I actually downloaded a recommended extension_

#### Network Settings

- Configure how Firefox connects to the internet: Use the defaults
  - _I haven't looked into customizing any of these settings yet_

### Home

#### Home

##### New Windows and Tabs

- Homepage and new windows: *Custom URLs...* `https://db.d11z.me/`
  - _It's not exactly production ready yet, but it's still better than most of the bloated homepages in most major browsers_
- New tabs: `Blank Page`
  - _Again, I'm not a fan of useless clutter.  I browse with intent and efficiency in mind_

##### Firefox Home Content

This section doesn't really matter since the home page is overridden above, but I uncheck all options here just to be thorough and consistent (I wouldn't want all that clutter on my homepage anyways).

### Search

#### Search

##### Search Bar

- Use the address bar for search and navigation: `true`
  - _It's a simpler, cleaner, and easier UI in my opinion_

##### Default Seach Engine

- Choose the default search engine to use in the address bar and search bar: `DuckDuckGo`
  - _Because privacy is more important than good search results... If you don't get good results, just use Google_
- Provide search suggestions: `false`
  - _No thanks, "Eye of Providence"_

##### One-Click Search Engines

- Remove all alternative search engines other than DuckDuckGo

### Privacy & Security

#### Browser Privacy

##### Content Blocking

- Manage Exceptions: Only add sites that you absolutely trust 100% to not serve you non-harmful content and don't sell your data
- Select *Standard* content blocking option, Firefox has good defaults
- Send websites a "Do Not Track" signal that you don't want to be tracked: `Always`
  - _I don't want any websites to track me in any way_

##### Cookies and Site Data

- "Clear Data..." first, and clear everything!
- "Manage Data..." should be empty after clearing all data
- "Manage Permissions..." allow or block any necessary sites
  - Example: Allow `https://www.dsthedev.com`
- Delete cookies and site data when Firefox is closed: `true`
  - _This all goes back to my "clean slate" policy, I'll save the things I want to keep around_

##### Logins & Passwords

- Ask to save logins and passwords for websites: `false`
- "Saved Logins..." remove any and all current
- Use a master password: `false`
  - _Just remember your logins and passwords, seriously_

##### History

- Firefox will: `Use custom settings for history`
  - Always use private browsing mode: false
    - "Clear History..." clear everything
  - Remember browsing and download history: `false`
  - Remember search and form history: `false`
  - Clear history when Firefox closes: `true`
    - "Settings..." clear everything
- _Clean slate yo!_

##### Address Bar

- When using the address bar, suggest: `Bookmarks` and nothing else
  - _No need for history, and I don't keep 75 tabs open_

#### Permissions

- Locations, Camera, Microphone, Notifications: Check the "Settings..." for each and clear them; sites will ask for permissions when necessary
- Block websites from automatically playing sound: `true`
  - _Excuse me, I'll choose when I want sound to play_
- Block pop-up windows: `true`
  - _What is this, 1998?_
- Warn you when websites try to install add-ons
  - _wtf, how is this even an option?!  It should be here's information about the what & why followed by ask for permission to install add-ons_
- Prevent accessibility services from accessing your browser: `false`
  - _Unless these services cause harm or interfere with my browsing experience, I see no reason to prevent using them_

#### Firefox Data Collection and Use

- Set all options to `false` for now until further research is done on this topic

#### Security

##### Deceptive Content and Dangerous Software Protection

- Set all to `true`

##### Certificates

- Use the default settings

### Firefox Account

Considering how private and locked down I have my settings, I don't use or recommend using their Sync feature.  It takes minutes to configure the settings and bookmarks can be easily exported (plus I don't use the same bookmarks on every device anyways).

---

## Resources

- [Do you allow pages to choose their own fonts?](https://old.reddit.com/r/firefox/comments/7yrt19/do_you_allow_pages_to_choose_their_own_fonts/)
- [Watch DRM content in Firefox?](https://support.mozilla.org/en-US/kb/enable-drm)

### Fun Resources

- [No thanks, "Eye of Providence"](https://en.wikipedia.org/wiki/Eye_of_Providence)

## TODO's

- [ ] Find a spell check extension to replace built-in spell check?
- [ ] Review the Applications preference entry to fully control how downloaded files are handled
- [ ] Review [Firefox's performance settings](https://support.mozilla.org/en-US/kb/performance-settings)
- [ ] Consider customizing the [Connection settings in Firefox](https://support.mozilla.org/en-US/kb/connection-settings-firefox)
- [ ] Go over [Firefox's Privacy Policy](https://www.mozilla.org/en-US/privacy/firefox/) to properly set [Data Collection and Use](#Firefox-Data-Collection-and-Use) settings above
- [ ] Look into the Security Settings more in depth, specifically for [Deceptive Content](https://support.mozilla.org/en-US/kb/how-does-phishing-and-malware-protection-work) and [Certificates](#Certificates)
