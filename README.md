ErrorLens turbo-charges the language diagnostic features, by making diagnostics stand out more prominently, highlighting
the entire line wherever a diagnostic is generated by the language and also prints the diagnostic message(s) in-line at
the site of the line of code which is generating the diagnostic.

![ErrorLens example](https://raw.githubusercontent.com/usernamehw/vscode-error-lens/master/img/demo.png)

## Features

* Highlight lines containing diagnostics
* Append diagnostic as text to the end of the line
* Show icons in gutter
* Show message in status bar

## Settings

<details>

<summary> Table of contributed settings:</summary>

| Name | Default | Description |
| --- | --- | --- |
| errorLens.fontSize | | Font size of annotations. (**HACK**) |
| errorLens.fontFamily | | Font family of annotations. (**HACK**) |
| errorLens.fontWeight | normal | Font Weight of annotations. |
| errorLens.fontStyleItalic | **false** | Show ErrorLens annotations in Italics, or not? |
| errorLens.margin | 30px | Distance between the end of the line and the start of annotation. (CSS units) |
| errorLens.padding | | Adds padding for the message. Visible difference when `message` colors are set. [Issue #23](https://github.com/usernamehw/vscode-error-lens/issues/23). Example: `2px 1ch`. |
| errorLens.borderRadius | 3px | Adds border-radius for the message. Visible difference when `message` colors are set. [Issue #23](https://github.com/usernamehw/vscode-error-lens/issues/23). Example: `5px`. |
| errorLens.enabledDiagnosticLevels | ["error","warning","info","hint"] | Customize which diagnostic levels to highlight. |
| errorLens.annotationPrefix | ["ERROR: ","WARNING: ","INFO: ","HINT: "] | Specify diagnostic message prefixes (when addAnnotationTextPrefixes is true). For example, emoji: ❗ ⚠ ℹ. |
| errorLens.addAnnotationTextPrefixes | **false** | When checked prefixes the diagnostic severity ('ERROR:', 'WARNING:' etc) to ErrorLens annotations. |
| errorLens.addNumberOfDiagnostics | **false** | When checked prefixes number of diagnostics on the line. Like: `[1/2]`. |
| errorLens.statusBarMessageEnabled | **false** | When checked shows current diagnostic in status bar. |
| errorLens.statusBarColorsEnabled | **false** | When checked - the extension uses decoration foreground as color of StatusBar text. |
| errorLens.exclude | [] | Specify messages that should not be highlighted (RegEx). |
| errorLens.delay | **0** | **EXPERIMENTAL** Specify delay before showing problems. |
| errorLens.onSave | **false** |  Update decorations only on document save. |
| errorLens.gutterIconsEnabled | **false** | Show gutter icons (In place of debug breakpoint icon). |
| errorLens.gutterIconsFollowCursorOverride | **true** | If this setting is `true` and `followCursor` setting is not `allLines`, then gutter icons would be rendered for all problems. But line decorations (background, message) only for active line." |
| errorLens.gutterIconSize | 100% | Customize gutter icon size. Example: `120%` |
| errorLens.gutterIconSet | default | Customize gutter icon style. Possible values: `default`, `defaultOutline`, `borderless`, `circle`. |
| errorLens.errorGutterIconPath | | Set custom icons for gutter. Absolute path for error gutter icon. |
| errorLens.warningGutterIconPath | | Set custom icons for gutter. Absolute path for warning gutter icon. |
| errorLens.infoGutterIconPath | | Set custom icons for gutter. Absolute path for info gutter icon. |
| errorLens.errorGutterIconColor | `#e45454` | Error color of the `circle` gutter icon set. |
| errorLens.warningGutterIconColor | `#ff942f` | Warning color of the `circle` gutter icon set. |
| errorLens.infoGutterIconColor | `#00b7e4` | Info color of the `circle` gutter icon set. |
| errorLens.followCursor | allLines | Highlight only portion of the problems. Possible values: `allLines`, `activeLine`, `closestProblem`. |
| followCursorMore | **0** | Augments `followCursor`. Adds number of lines to top and bottom when `followCursor` is `activeLine`. Adds number of closest problems when `followCursor` is `closestProblem` |

</details>

## Commands

* `errorLens.toggle` Temporarily Enable/Disable ErrorLens.
* `errorLens.toggleError` Temporarily Enable/Disable Error level.
* `errorLens.toggleWarning` Temporarily Enable/Disable Warning level.
* `errorLens.toggleInfo` Temporarily Enable/Disable Info level.
* `errorLens.toggleHint` Temporarily Enable/Disable Hint level.
* `errorLens.copyProblemMessage` Copy problem message to clipboard (at the active line).

## Colors

Can be configured in `settings.json` (**`workbench.colorCustomizations`** section)

| Name | Light | Dark |
| --- | --- | --- |
| errorLens.errorBackground | `#e4545420` | `#e454541b` |
| errorLens.errorForeground | `#e45454` ![](https://placehold.it/15/e45454?text=+) | `#ff6464` |
| errorLens.errorMessageBackground | `#fff0` | `#fff0` |
| errorLens.warningBackground | `#ff942f20` | `#ff942f1b`|
| errorLens.warningForeground | `#ff942f` ![](https://placehold.it/15/ff942f?text=+) | `#fa973a` |
| errorLens.warningMessageBackground | `#fff0` | `#fff0` |
| errorLens.infoBackground | `#00b7e420` | `#00b7e420` |
| errorLens.infoForeground | `#00b7e4` ![](https://placehold.it/15/00b7e4?text=+) | `#00b7e4` |
| errorLens.infoMessageBackground | `#fff0` | `#fff0` |
| errorLens.hintBackground | `#17a2a220` | `#17a2a220` |
| errorLens.hintForeground | `#2faf64` ![](https://placehold.it/15/2faf64?text=+) | `#2faf64` |
| errorLens.hintMessageBackground | `#fff0` | `#fff0` |

## [Miscellaneous: `misc.md`](https://github.com/usernamehw/vscode-error-lens/blob/master/misc.md)
