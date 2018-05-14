# Visual Studio Code

1. [Download](https://code.visualstudio.com/Download) & run installer
	1. Install on main drive, as performance is important
	2. Enable "Open with Code" options (2) and add to PATH

## Extensions

```bash
code --install-extension albymor.increment-selection
code --install-extension bradgashler.htmltagwrap
code --install-extension christian-kohler.npm-intellisense
code --install-extension DavidAnson.vscode-markdownlint
code --install-extension esbenp.prettier-vscode
code --install-extension felixfbecker.php-debug
code --install-extension gerane.Theme-azure
code --install-extension glen-84.sass-lint
code --install-extension helixquar.randomeverything
code --install-extension johnstoncode.svn-scm
code --install-extension mkloubert.vscode-deploy-reloaded
code --install-extension mrmlnc.vscode-apache
code --install-extension ms-mssql.mssql
code --install-extension ms-vscode.PowerShell
code --install-extension PKief.material-icon-theme
code --install-extension steve8708.Align
code --install-extension Tyriar.sort-lines
code --install-extension yzhang.markdown-all-in-one
code --install-extension zhuangtongfa.Material-theme
```

### Extension Resources

- [Prettier](https://prettier.io/docs/en/configuration.html)

## User Settings

```json
{
  "workbench.startupEditor": "none",
  // "markdown.extension.preview.autoShowPreviewToSide": true,
  "workbench.colorTheme": "One Dark Pro",
  "workbench.iconTheme": "material-icon-theme",
  "editor.fontFamily":
    "'Fira Code', 'Source Code Pro ExtraLight', 'Courier New', monospace",
  "editor.fontSize": 14,
  "editor.fontLigatures": true,
  "editor.cursorStyle": "line-thin",
  "editor.insertSpaces": false,
  "editor.cursorBlinking": "phase",
  "editor.renderControlCharacters": true,
  "editor.rulers": [40, 80, 120],
  "editor.smoothScrolling": true,
  "explorer.autoReveal": false,
  "window.menuBarVisibility": "toggle",
  "files.trimFinalNewlines": true,
  "files.trimTrailingWhitespace": true,
  "explorer.sortOrder": "type",
  "editor.tabSize": 2,
  "php.validate.executablePath": "E:/MAMP/bin/php/php7.1.5/php.exe",
  "files.associations": {
    "*.lmo": "html" // Libercus template's language mixes with HTML
  },
  "markdownlint.config": {
    "MD010": false
  },
  "editor.renderWhitespace": "all",
  "explorer.confirmDelete": false,
  "window.zoomLevel": 0,
  "editor.tabCompletion": false,
  "files.autoSave": "off"
}
```

## Keyboard Shortcuts

- Extension marketplace: `ctrl+shift+x`
- Settings: `ctrl+,`
- Terminal/Powershell: `ctrl+`\`
- Duplicate Line: `alt+shift+up|down`
- Keyboard Shortcut Viewer: `ctrl+k>s`
- Open Workspace: `ctrl+l>o` (Custom)

## Custom Keybindings

```json
[
  {
    "key": "ctrl+l ctrl+o",
    "command": "workbench.action.openWorkspace"
  },
  {
    "key": "ctrl+l ctrl+s",
    "command": "workbench.action.openSnippets"
  },
  {
    "key": "ctrl+shift+r",
    "command": "workbench.files.action.refreshFilesExplorer"
  },
  {
    "key": "ctrl+shift+u",
    "command": "editor.action.transformToUppercase",
    "when": "editorTextFocus"
  },
  {
    "key": "ctrl+shift+l",
    "command": "editor.action.transformToLowercase",
    "when": "editorTextFocus"
  }
]
```

## Snippets

### Global

```json
{
  "New Junction Link (Psuedo-Symbolic `ln -s`)": {
    "prefix": "mklink",
    "body": ["mklink /J $1 $2"],
    "description":
      "For CMD prompt only, creates a symbolic link at $1:LinkDir from $2:RealDir"
  },
  "Windows Symbolic Link": {
    "prefix": "symlink",
    "body": ["New-Item -Path $1 -ItemType SymbolicLink -Value $2"],
    "description":
      "For PowerShell, requires Developer mode enabled, Create a symbolic link at $1:LinkDir from $2:RealDir"
  }
}
```

### HTML

```json
{
	"PHP Tags": {
		"prefix": "php",
		"body": [
			"<?php $2${1: ?>}",
		],
		"description": "Creates an opening and closing php tag."
	}
}
```

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
      "}"
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
      " */"
    ],
    "description": "Simple DocComment by dsthedev"
  }
}
```

### SCSS

```json
{
  "Media Query | Foundation 6": {
    "prefix": "fn mediaquery",
    "body": [
      "@include breakpoint( ${1:medium} ${2: down|only }) {",
      "\t$3",
      "}"
    ],
    "description":
      "Create a responsive breakpoint to customize the Foundation framework."
  }
}
```

## First Impressions

- Start screen is nice; start, recent, help, customize, and learn are all useful
- Built in keyboard shortcut cheat sheet with search is amazing
- Built in terminal/powershell? Awesome, no need for gitbash anymore

## License

- Between Microsoft Corporation and you
- Terms apply to software, services, updates; except for exceptions
- Installation and Use
  - May use any number of copies, even for corporate
  - May use for demonstrations
  - You can make a backup copy of the software
  - Third Party Programs
    - Even if they have agreements, the disclaimers and rules of this agreement still apply
    - This software includes 3rd party components, and for $5 source code can be made available from Microsoft
  - Extensions
    - 3rd party extensions available via the marketplace have their own agreements and licensing which Microsoft is not responsible for
- Data
  - @todo: finish reading & summarizing license, which should be done before installation usually!

## Thoughts

- The git integration is super nice, but the commands and branch management are kind of weird
- I wonder if I can automate my VSCode configuration with a bash or powershell script?
