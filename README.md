<div align="center">
  <img src="icon.png" alt="Zenith Icon" width="128">
  <h1>Zenith Theme for VS Code</h1>
  <p><strong>A refined theme that balances minimal design with a clear visual hierarchy.</strong></p>
  <br>
</div>

![Zenith Screenshot](screenshot.png)

## Installation

1. Install theme from the VS Code Marketplace ([direct link](https://marketplace.visualstudio.com/items?itemName=britown.vscode-theme-zenith))
2. Set your `Color Theme` to `Zenith`
3. Set your `File Icon Theme` to `Zenith` for file icons that match the theme colors
4. (Optional) Apply the suggested settings below

## Suggested settings

**Font**

The font in the screenshot is [JetBrains Mono](https://www.jetbrains.com/lp/mono/) with these these settings:

```json
"editor.fontFamily": "'JetBrains Mono'",
"editor.fontLigatures": true, // If you want ligatures
"editor.fontSize": 13,

"terminal.integrated.fontFamily": "'JetBrains Mono'",
"terminal.integrated.fontLigatures": true // If you want ligatures
"terminal.integrated.fontSize": 13,
"terminal.integrated.lineHeight": 1.1,
```

**UI Elements**

```json
// Tone down the use of colors in Explorer and Editor:
"explorer.decorations.colors": false,
"outline.problems.colors": false,
"workbench.editor.decorations.colors": false,
"editor.bracketPairColorization.enabled": false

// Align icons in Explorer, adjust width of resize indicators, extend editor line highlight into gutter
"workbench.tree.indent": 18,
"workbench.tree.renderIndentGuides": "none",
"workbench.sash.size": 2,
"editor.renderLineHighlight": "all",
```

**Extensions**

Apply these you use the following extensions:

```json
"errorLens.borderRadius": "4px",
"errorLens.margin": "2ch",
"errorLens.messageBackgroundMode": "message",
"errorLens.padding": "1px 5px",

"gitlens.currentLine.fontStyle": "italic",
```

**Other**

All of the theme-related and layout tweaks I use can be found in [suggested-settings.jsonc](https://github.com/bkuzmanoski/vscode-theme-zenith/blob/main/suggested-settings.jsonc) for easy copy-and-pasting.

## Customization

**Add a blue accent to the top active editor tabs**

```json
"workbench.colorCustomizations": {
    "tab.activeBorderTop": "#61abda"
},
```

**Remove the border around matching bracket pairs**

```json
"workbench.colorCustomizations": {
    "editorBracketMatch.border": "#00000000",
    "editorBracketMatch.background": "#ccebff28" // Highlight their background color instead
},
```

**Highlight quotation marks/backticks surrounding strings in green**

```json
"editor.tokenColorCustomizations": {
  "textMateRules": [
    {
      "scope": [
        "punctuation.definition.string",
        "punctuation.definition.raw"
      ],
      "settings": {
        "foreground": "#64b280"
      }
    }
  ]
},
```

## Acknowledgments

- The syntax highlighting colors were inspired by the "zenwritten_dark" Ghostty theme ([mbadolato/iTerm2-Color-Schemes](https://github.com/mbadolato/iTerm2-Color-Schemes)) which was in turn taken from [mcchrish/zenbones.nvim](https://github.com/mcchrish/zenbones.nvim)
- The File Icon Theme uses the Seti UI icons ([jesseweed/seti-ui](https://github.com/jesseweed/seti-ui))

## Bonus themes

- Ghostty: [ghostty-theme-zenith.md](https://gist.github.com/bkuzmanoski/b0b310a77a8e9b9891f84af2712ad87b)
- micro (CLI editor): [micro-theme-zenith.md](https://gist.github.com/bkuzmanoski/592c0cd8ba082e842e65630c44290ae7)

---

Found a bug or have a request? Please [open an issue](https://github.com/bkuzmanoski/vscode-theme-zenith/issues).
