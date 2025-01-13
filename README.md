<img src="icon.png" alt="Zenith Icon" width="128">

# Zenith Theme for Visual Studio Code

**A refined blue-gray theme that balances minimal design with a clear visual hierarchy.**

Zenith uses subtle contrasts and thoughtful color choices reduce eye strain and maintain excellent readability for long coding sessions.

![Zenith Screenshot](screenshot.png)

- Comprehensive UI coverage for a cohesive experience (Extensions, Settings, Testing, Run and Debug, and other views included)
- Syntax highlighting with [semantic highlighting](https://code.visualstudio.com/api/language-extensions/semantic-highlight-guide) enabled
- File icons that match the theme colors
- Theming for the [Error Lens](https://marketplace.visualstudio.com/items?itemName=usernamehw.errorlens) and [GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot) extensions (if you use them)

## Installation

1. Install Zenith Theme from the Visual Studio Marketplace ([direct link](https://marketplace.visualstudio.com/items?itemName=britown.vscode-theme-zenith))
2. Go to `View → Command Palette`, type `Color Theme` and press enter, then select `Zenith`
3. Go to `View → Command Palette`, type `File Icon Theme` and press enter, then select `Zenith`
4. (Optional) Apply the suggested User Settings below

## Suggested User Settings

Try the following Visual Studio Code settings for a more minimal and aesthetic experience.

To apply the settings below, go to `View → Command Palette`, type `Open User Settings (JSON)` and press enter, then paste the settings you want to try in your `settings.json` file. [Click here](https://github.com/bkuzmanoski/vscode-theme-zenith/blob/main/suggested-settings.jsonc) to view a single file that contains all of the suggested settings for easier copy-and-pasting.

### Fonts

The font used in the screenshot above is [JetBrains Mono](https://www.jetbrains.com/lp/mono/). After you install it on your computer, apply the these settings:

```json
  "editor.fontFamily": "'JetBrains Mono'",
  "editor.fontLigatures": "'liga'",
  "editor.fontSize": 13,
  "editor.letterSpacing": 0.1,

  "terminal.integrated.fontFamily": "'JetBrains Mono', monospace",
  "terminal.integrated.fontLigatures": true,
  "terminal.integrated.fontSize": 13,
  "terminal.integrated.lineHeight": 1.1,
```

### Aesthetics (Part 1: Look and Feel)

```json
  "editor.cursorWidth": 1,
  "editor.find.addExtraSpaceOnTop": false,
  "editor.roundedSelection": false,
  "editor.renderLineHighlight": "all",

  "explorer.decorations.colors": false,

  "outline.problems.colors": false,

  "terminal.integrated.drawBoldTextInBrightColors": false,
  "terminal.integrated.minimumContrastRatio": 1,

  "workbench.editor.decorations.colors": false,
  "workbench.editor.titleScrollbarSizing": "large",
  "workbench.sash.size": 2,
  "workbench.tree.indent": 18,
```

### Aesthetics (Part 2: Minimize Visual Noise)

These settings hide various UI elements that otherwise make Visual Studio Code feel cluttered:

```json
  "chat.commandCenter.enabled": false, // If you have GitHub Copilot installed

  "editor.bracketPairColorization.enabled": false,

  "terminal.integrated.shellIntegration.decorationsEnabled": "overviewRuler",
  "terminal.integrated.shellIntegration.showCommandGuide": false,

  "workbench.editor.empty.hint": "hidden",
  "workbench.layoutControl.enabled": false,
  "workbench.startupEditor": "none",
  "workbench.tree.renderIndentGuides": "none",
```

- **Note**: Setting `workbench.layoutControl.enabled` to `false` will hide the Sidebar and Panel toggles at the top-right of your window. The [keyboard shortcuts](https://code.visualstudio.com/docs/getstarted/keybindings#_keyboard-shortcuts-reference) for these are way more convenient anyway 😉.
- **Note**: Sidebar views, Sidebar sections, Panel views, and Status Bar items cannot be hidden via User Settings. Right click on any that don't ⭐spark joy⭐ and select `Hide`.

### Controversial Choices

Apply these settings to taste. I like them, but you may not 😇.

```json
  "breadcrumbs.enabled": false,

  "editor.minimap.enabled": false,
  "editor.scrollbar.horizontal": "hidden",

  "terminal.integrated.cursorBlinking": true,
  "terminal.integrated.cursorStyle": "line",
  "terminal.integrated.cursorStyleInactive": "none",
  "terminal.integrated.cursorWidth": 1,
```

### Error Lens Tweaks

If you have the Error Lens extension installed, these settings might be useful:

```json
  "errorLens.borderRadius": "4px",
  "errorLens.margin": "2ch",
  "errorLens.messageBackgroundMode": "message",
  "errorLens.padding": "1px 5px",
```

## Customization

You can customize any colors you aren't vibing with (see the [customization guide](https://code.visualstudio.com/api/references/theme-color) for details). For example, this setting will add a blue accent to the top active editor tabs:

```json
"workbench.colorCustomizations": {
    "tab.activeBorderTop": "#61abda",
}
```

## Acknowledgments

- The syntax highlighting colors were inspired by the [Ghostty](https://ghostty.org/) "zenwritten_dark" theme ([mbadolato/iTerm2-Color-Schemes](https://github.com/mbadolato/iTerm2-Color-Schemes))...
- ...which was in turn taken from [mcchrish/zenbones.nvim](https://github.com/mcchrish/zenbones.nvim)
- The File Icon Theme is based on the Seti UI icons ([jesseweed/seti-ui](https://github.com/jesseweed/seti-ui))

**Bonus**: If you use Ghostty and want a matching theme, look here: [ghostty-theme-zenith.md](https://gist.github.com/bkuzmanoski/b0b310a77a8e9b9891f84af2712ad87b).

## Contributing

Found a bug or have a request? Please [open an issue](https://github.com/bkuzmanoski/vscode-theme-zenith/issues).

## Changelog

See [CHANGELOG.md](https://github.com/bkuzmanoski/vscode-theme-zenith/blob/main/CHANGELOG.md) for details.
