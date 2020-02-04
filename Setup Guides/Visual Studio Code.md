# Visual Studio Code

## Installation

### Windows / Mac Install

1. [Download VSCode Installer](https://code.visualstudio.com/Download)
2. Run the installer
3. `cmd+shift+p` & `Shell Command: Install 'code' command in PATH`

### Linux / Pop!_OS 19.10

```bash
sudo apt install software-properties-common apt-transport-https wget -y # Install dependencies
wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add - # Import Microsoft's GPG key
sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main" # Enable VSCode repository
sudo apt update
sudo apt install code
## Install VSCode extensions
```

## Settings (JSON)

The most up to date version of my settings are [here](https://gist.github.com/dsthedev/4a8dcf92bc7771498a1950276f12b2a5).

```json
{
    "editor.fontSize": 12,
    "editor.fontFamily": "Fira Code, Menlo, Monaco, 'Courier New', monospace",
    "editor.cursorStyle": "line-thin",
    "editor.multiCursorModifier": "ctrlCmd",
    "editor.insertSpaces": false,
    "workbench.startupEditor": "none",
    "editor.fontLigatures": true,
    "editor.cursorBlinking": "phase",
    "terminal.integrated.cursorBlinking": true,
    "editor.renderWhitespace": "boundary",
    "window.openFoldersInNewWindow": "on",
    "files.trimTrailingWhitespace": true,
    "files.trimFinalNewlines": true,
    "explorer.sortOrder": "type",
    "editor.tabSize": 2,
    "workbench.editor.highlightModifiedTabs": true,
    "workbench.fontAliasing": "antialiased",
    "editor.fontWeight": "200"
}
```

## Shortcuts

| Command                 | Purpose                                                |
| ---:                    | ---                                                    |
| `cmd+shift+\`           | Find/bounce between end/start brackets                 |
| `cmd+option+left/right` | Switch tabs l/r                                        |
| `ctrl+cmd+left/right`   | Move tab to next/prev window                           |
| `cmd+b`                 | show/hide the sidebar (doesn't work in markdown files) |
| `option+z`              | Toggle wordwrap                                        |
| `alt+shift+up|down`     | Duplicate Line                                         |
| `ctrl+k>s`              | Keyboard Shortcut Viewer                               |
| `ctrl+g                 | Jump to line                                           |

## Extensions

| Name                      | URL                              |
| ---:                      | ---                              |
| Markdown All in One       | `yzhang.markdown-all-in-one`     |
| markdownlint              | `davidanson.vscode-markdownlint` |
| Prettier - Code formatter | `esbenp.prettier-vscode`         |
| PHP DocBlocker            | `neilbrayfield.php-docblocker`   |
| Transformer               | `dakara.transformer`             |
| Simple Alignment          | `earshinov.simple-alignment`     |
| One Dark Pro              | `zhuangtongfa.material-theme`    |

## TODO

- Create a bash script that installs all my extensions

---
## **IGNORE EVERYTHING BELOW, IT'S ONLY THERE FOR REFERENCE WHILE I REBUILD THIS DOC!**
---

## Extensions

**Gist:** [vsc-extensions.sh](https://gist.github.com/dsthedev/43124de9436065086605b33a311bebf6)

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

## User Settings

**Gist:** [vsc-user-settings.json](https://gist.github.com/dsthedev/4a8dcf92bc7771498a1950276f12b2a5)

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

## Custom Keybindings

**Gist:** [vsc-custom-keybindings.json](https://gist.github.com/dsthedev/d8bb62feac45419662107d8a87f259f4)

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
