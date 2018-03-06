# Visual Studio Code

1. [Download](https://code.visualstudio.com/Download) & run installer
   1. Install on main drive, as performance is important
   2. Enable "Open with Code" options (2) and add to PATH

## Extensions

* [Markdown All in One](https://github.com/neilsustc/vscode-markdown)
  * Enable auto preview
* [htmltagwrap](https://github.com/bgashler1/vscode-htmltagwrap)
* [markdownlint](https://github.com/mkloubert/vscode-deploy-reloaded)
* [Nomo Dark Icon Theme](https://github.com/be5invis/vscode-iconset)
* [Deploy (Reloaded)](https://github.com/mkloubert/vscode-deploy-reloaded)

## Keyboard Shortcuts

* Extension marketplace: `ctrl+shift+x`
* Settings: `ctrl+,`
* Terminal/Powershell: `ctrl+`\`
* Duplicate Line: `alt+shift+up|down`
* Keyboard Shortcut Viewer: `ctrl+k>s`
* Open Workspace: `ctrl+l>o` (Custom)

## Custom Keybindings

```json
[
    { "key": "ctrl+l ctrl+o",    "command": "workbench.action.openWorkspace" },
]
```

## User Settings

```json
{
    "workbench.startupEditor": "newUntitledFile",
    "markdown.extension.preview.autoShowPreviewToSide": true,
    "workbench.colorTheme": "Sea Green Theme",
    "workbench.iconTheme": "vs-nomo-dark",
    "editor.fontFamily": "'Source Code Pro', 'Courier New', monospace",
    "editor.fontSize": 14,
    "editor.cursorStyle": "line-thin",
    "editor.insertSpaces": false,
    "editor.cursorBlinking": "phase",
    "editor.renderControlCharacters": true,
    "editor.rulers": [40,80,120],
    "editor.smoothScrolling": true,
    "window.menuBarVisibility": "toggle",
    "files.trimFinalNewlines": true,
    "files.trimTrailingWhitespace": true,
    "explorer.sortOrder": "type",
    "editor.tabSize": 2,
}
```

## Snippets

### PHP

```json
{
	"PHP Class | dsthedev": {
		"prefix": "class",
		"body": [
			"/**",
			" * ${1:ClassName} - ${2:Class Summary}${4:",
			" *",
			" * @${3:param details}}",
			" */",
			"class ${1:ClassName} {",
				"\t$5",
			"}",
		],
		"description": "Simple PHP Class by dsthedev"
	},
	"DocComment | dsthedev": {
		"prefix": "doccomment",
		"body": [
			"/**",
			" * ${1:Summary}${3:",
			" *",
			" * @${2:param details}}",
			" */",
		],
		"description": "Simple DocComment by dsthedev"
	}
}
```

## First Impressions

* Start screen is nice; start, recent, help, customize, and learn are all useful
* Built in keyboard shortcut cheat sheet with search is amazing
* Built in terminal/powershell?  Awesome, no need for gitbash anymore

## License

* Between Microsoft Corporation and you
* Terms apply to software, services, updates; except for exceptions
* Installation and Use
  * May use any number of copies, even for corporate
  * May use for demonstrations
  * You can make a backup copy of the software
  * Third Party Programs
    * Even if they have agreements, the disclaimers and rules of this agreement still apply
    * This software includes 3rd party components, and for $5 source code can be made available from Microsoft
  * Extensions
    * 3rd party extensions available via the marketplace have their own agreements and licensing which Microsoft is not responsible for
* Data
  * @todo: finish reading & summarizing license, which should be done before installation usually!

## Thoughts

* The git integration is super nice, but the commands and branch management are kind of weird
* I wonder if I can automate my VSCode configuration with a bash or powershell script?
