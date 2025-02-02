<div align="center">
  <img src="assets/icon-transparent.png" alt="Zenith Icon" width="128">
  <h1>Zenith Theme for VS Code</h1>
  <p>
    <strong>A refined dark theme with cohesive colors and complete UI coverage.</strong>
    <br>
    Check out the ⭐ light theme ⭐ here: <a href="https://marketplace.visualstudio.com/items?itemName=britown.vscode-theme-meridian">Meridian Theme for VS Code</a>.
  </p>
  <br>
</div>

![Zenith Screenshot](assets/screenshot.png)

## Installation

1. Install theme from the VS Code Marketplace ([direct link](https://marketplace.visualstudio.com/items?itemName=britown.vscode-theme-zenith))
2. Set your `Color Theme` to `Zenith`
3. Set your `File Icon Theme` to `Zenith` for file icons that match the theme colors
4. (Optional) Apply the suggested settings below

## Suggested settings

**Font**

The font in the screenshot is [JetBrains Mono](https://www.jetbrains.com/lp/mono/) with these these settings:

```json
"editor.fontFamily": "JetBrains Mono",
"editor.fontLigatures": true, // If you want ligatures
"editor.fontSize": 13,

"terminal.integrated.fontFamily": "JetBrains Mono",
"terminal.integrated.fontLigatures": true // If you want ligatures
"terminal.integrated.fontSize": 13,
"terminal.integrated.lineHeight": 1.1,
```

**UI elements**

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
"errorLens.padding": "1px 4px",

"gitlens.currentLine.fontStyle": "italic",
```

**Other**

All of the theme-related and layout tweaks I use can be found in [suggested-settings.json](https://github.com/bkuzmanoski/vscode-theme-zenith/blob/main/suggested-settings.json) for easy copy-and-pasting.

## Customization

**Add a blue accent to the top active editor tabs**

```json
"workbench.colorCustomizations": {
  "[Zenith]": {
    "tab.activeBorderTop": "#61abda"
  }
},
```

**Remove the border around matching bracket pairs**

```json
"workbench.colorCustomizations": {
  "[Zenith]": {
    "editorBracketMatch.border": "#00000000",
    "editorBracketMatch.background": "#ccebff28" // Highlight their background color instead
  }
},
```

**Highlight quotation marks/backticks surrounding strings in green**

```json
"editor.tokenColorCustomizations": {
  "[Zenith]": {
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
},
```

## Zenith theme for other apps

Check out the matching [Raycast theme](https://themes.ray.so?version=1&name=Zenith&author=Brian%20Kuzmanoski&authorUsername=britown&colors=%23161A1D,%23161A1D,%23B4BBC2,%23B4BBC2,%2361ABDA,%23DE6E7C,%23D68C67,%23D6B867,%2364B280,%2361ABDA,%239D86CE,%23CF86C1&appearance=dark&addToRaycast) and visit my [dotfiles repo](https://github.com/bkuzmanoski/dotfiles) for ports of this theme for **bat**, **btop**, **eza**, **Ghostty**, **micro**, and **zsh-syntax-highlighting**.

## Acknowledgments

The syntax highlighting colors were inspired by the "zenwritten_dark" Ghostty theme ([mbadolato/iTerm2-Color-Schemes](https://github.com/mbadolato/iTerm2-Color-Schemes)) which was in turn taken from [mcchrish/zenbones.nvim](https://github.com/mcchrish/zenbones.nvim).

The file icon theme uses the Seti UI icons ([jesseweed/seti-ui](https://github.com/jesseweed/seti-ui)).

---

Found a bug or have a request? Please [open an issue](https://github.com/bkuzmanoski/vscode-theme-zenith/issues).
