# VS Code

### Open project on VS Code
```bash
cd 'project path'
code .
```

### Shortcuts

#### Copy line
<kbd>Shift</kbd> + <kbd>Option</kbd> + <kbd>Down</kbd> or <kbd>Up</kbd>

#### PDF
- [Mac OS](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf)
- [Windows](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)


### Extensions (Marketplace)
- [Auto Import by steoates](https://marketplace.visualstudio.com/items?itemName=steoates.autoimport)
- [Angular v6 Snippets by John Para](https://marketplace.visualstudio.com/items?itemName=johnpapa.Angular2)
- [Auto Close Tag by Jun Han](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag)
- [Auto Rename Tag by Jun Han](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag)
- [Live Server by Ritwick Dey](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
- [Beautify by HookyQR](https://marketplace.visualstudio.com/items?itemName=HookyQR.beautify)
- [Import cost](https://marketplace.visualstudio.com/items?itemName=wix.vscode-import-cost)
- [Highlight Matching Tag](https://marketplace.visualstudio.com/items?itemName=vincaslt.highlight-matching-tag)
- [Polacode](https://marketplace.visualstudio.com/items?itemName=pnp.polacode)
- [VSCode IntelliSense TailwindCSS](https://marketplace.visualstudio.com/items?itemName=bradlc.vscode-tailwindcss)

### Settings
```
{
  "editor.fontFamily": "Andale Mono, Operator Mono, Menlo, Monaco, 'Courier New', monospace",
  "editor.fontLigatures": true,
  "workbench.fontAliasing": "antialiased",
  "breadcrumbs.enabled": true,
  "workbench.colorTheme": "Super One Dark",
  "editor.fontSize": 13,
  "terminal.integrated.fontSize": 13,
  "files.associations": {
    "*.js": "javascriptreact"
  },
  "javascript.implicitProjectConfig.experimentalDecorators": true,
  "editor.tokenColorCustomizations": {
    "textMateRules": [
      {
        "scope": [
          //following will be in italic (=FlottFlott)
          "comment",
          "entity.name.type.class", //class names
          "keyword", //import, export, return…
          "constant", //String, Number, Boolean…, this, super
          "storage.modifier", //static keyword
          "storage.type.class.js", //class keyword
        ],
        "settings": {
          "fontStyle": "italic"
        }
      },
      {
        "scope": [
          //following will be excluded from italics (VSCode has some defaults for italics)
          "invalid",
          "keyword.operator",
          "constant.numeric.css",
          "keyword.other.unit.px.css",
          "constant.numeric.decimal.js",
          "constant.numeric.json"
        ],
        "settings": {
          "fontStyle": ""
        }
      }
    ]
  }
}
```
