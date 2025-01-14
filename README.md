<div align="center">
  <img src="icon.png" alt="Zenith Icon" width="128">
  <h1>Zenith Theme for VS Code</h1>
  <p><strong>A refined blue-gray theme that balances minimal design with a clear visual hierarchy.</strong></p>
  <br>
</div>

Zenith uses subtle contrasts and thoughtful color choices reduce eye strain and maintain readability for long coding sessions.

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
"editor.fontSize": 13,
"editor.letterSpacing": 0.1,
"editor.fontLigatures": "'liga'", // If you want ligatures

"terminal.integrated.fontFamily": "'JetBrains Mono', monospace",
"terminal.integrated.fontSize": 13,
"terminal.integrated.lineHeight": 1.1,
"terminal.integrated.fontLigatures": true // If you want ligatures
```

**Colors**

Tone down the use of colors in Explorer and Editor:

```json
"explorer.decorations.colors": false,
"outline.problems.colors": false,
"workbench.editor.decorations.colors": false,
"editor.bracketPairColorization.enabled": false // If you prefer more minimal syntax highlighting
```

**Layout**

Align icons in Explorer and hide guides/decorations in Terminal:

```json
"workbench.sash.size": 2,
"workbench.tree.indent": 18,
"workbench.tree.renderIndentGuides": "none",
"editor.renderLineHighlight": "all",
"terminal.integrated.shellIntegration.decorationsEnabled": "overviewRuler",
"terminal.integrated.shellIntegration.showCommandGuide": false
```

**Error Lens**

If you use the [Error Lens](https://marketplace.visualstudio.com/items?itemName=usernamehw.errorlens) extension:

```json
"errorLens.borderRadius": "4px",
"errorLens.margin": "2ch",
"errorLens.messageBackgroundMode": "message",
"errorLens.padding": "1px 5px"
```

**Other**

See the above settings and other theme-related tweaks I use in [suggested-settings.jsonc](https://github.com/bkuzmanoski/vscode-theme-zenith/blob/main/suggested-settings.jsonc).

## Customization

**Add a blue accent to the top active editor tabs**

```json
"workbench.colorCustomizations": {
    "tab.activeBorderTop": "#61abda"
}
```

**Remove the border around matching bracket pairs**

```json
"workbench.colorCustomizations": {
    "editorBracketMatch.border": "#00000000",
    "editorBracketMatch.background": "#ccebff28" // Highlight their background color instead
}
```

**Remove italics in syntax highlighting**

```json
"editor.tokenColorCustomizations": {
  "textMateRules": [
    {
      "scope": [
        "comment",
        "keyword.operator.expression",
        "keyword.operator.new",
        "keyword",
        "meta.selector.pseudo-class punctuation.definition.entity",
        "meta.selector.pseudo-class",
        "meta.selector.pseudo-element punctuation.definition.entity"
        "meta.selector.pseudo-element",
        "punctuation.definition.comment",
        "punctuation.definition.keyword",
        "storage",
        "support.other",
        "variable.language"
      ],
      "settings": {
        "fontStyle": ""
      }
    }
  ]
}
```

**Highlight quotation marks and backticks surrounding strings/string literals in green**

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
}
```

**Other**

See the VS Code [theme customization guide](https://code.visualstudio.com/api/references/theme-color) for all of the possible overrides.

## Acknowledgments

- The syntax highlighting colors were inspired by the "zenwritten_dark" Ghostty theme ([mbadolato/iTerm2-Color-Schemes](https://github.com/mbadolato/iTerm2-Color-Schemes)) which was taken from [mcchrish/zenbones.nvim](https://github.com/mcchrish/zenbones.nvim)
- The File Icon Theme uses the Seti UI icons ([jesseweed/seti-ui](https://github.com/jesseweed/seti-ui))

**Bonus**: If you use Ghostty and want a matching theme, look here: [ghostty-theme-zenith.md](https://gist.github.com/bkuzmanoski/b0b310a77a8e9b9891f84af2712ad87b).

---

Found a bug or have a request? Please [open an issue](https://github.com/bkuzmanoski/vscode-theme-zenith/issues).
