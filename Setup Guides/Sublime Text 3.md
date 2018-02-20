# Setting Up Sublime Text 3

* Installation options
  * Add to explorer context menu
* Pin to Start
* Install [Package Manager](https://packagecontrol.io/installation)
* Add the following packages:
  * Theme - Cyanide
    * Make sure to update the theme and color scheme (Acid Contrasted)
    * See User Settings below
  * gitignore
  * PowerShell
  * SFTP
  * SVN
  * More Layouts - `alt + shift + 0`
  * SCSS
  * HTMLBeautify
  * Increment Selection
* Take note of the Packages folder for the install:
  * ​


## Keymappings

Replace `ctrl` with `cmd` if on OSX.

```
[
	{"keys": ["ctrl+alt+p"], "command": "prompt_select_workspace"},
	{"keys": ["ctrl+shift+y"], "command": "unexpand_tabs", "args": { "set_translate_tabs": true } },
	{"keys": ["ctrl+alt+s"], "command": "new_snippet" }
]
```

## Mouse Mapping

I really can't stand that the mouse wheel will change the font size, so to disable do the  following:

1. Create a new file called `Default (Windows).sublime-mousemap` in `C:\Users\\~Username~\AppData\Roaming\Sublime Text 3\Packages\User\`
2. Add this snippet to the newly created file:

```
[
  // Change font size with ctrl+scroll wheel
  { "button": "scroll_down", "modifiers": ["ctrl"], "command": "null" },
  { "button": "scroll_up", "modifiers": ["ctrl"], "command": "null" }
]
```

3. Enjoy not accidentally zooming the file size!

## Settings - User

```
{
	"caret_style": "phase",
	"color_scheme": "Packages/Theme - Cyanide/Cyanide - Acid - Contrasted.tmTheme",
	"default_line_ending": "unix",
	"draw_white_space": "all",
	"font_face": "Source Code Pro Light",
	"font_size":10,
	"highlight_line": true,
	"icon_file_type_enable": true,
	"ignored_packages":
	[
		"Vintage"
	],
	"large_scroll_bars": true,
	"match_brackets_angle": true,
	"rulers":
	[
		40,
		80,
		120
	],
	"spacefunk_folder_icons": true,
	"tab_size": 2,
	"theme": "Cyanide.sublime-theme",
	"translate_tabs_to_spaces": false,
	"trim_trailing_white_space_on_save": true,
	"wrap_width": 80
}
```

## Misc Settings

Open custom file extensions with existing syntax, like using the `.html` syntax for `.lmo` files.

1. Use the Menu to do it: `View -> Syntax -> Open all with current extension as ...`
2. Create a file called `syntax.sublime-settings` such as `HTML.sublime-settings` and add something similar to this:

```json
{
	"extensions":
	[
		"html",
		"htm",
		"html.erb",
		"lmo" // This is the new file to be highlighted like html files
	]
}
```

