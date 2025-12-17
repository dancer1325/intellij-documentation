[//]: # (Source: https://www.jetbrains.com/help/idea/pro-tips.html)
[//]: # (Downloaded: 2025-12-17 19:56:03)

## Coding assistance

### Full Line code completion

The [Full Line code completion](full-line-code-completion.html) feature uses a locally run deep learning model to suggest entire lines of code.

  * To accept an entire suggestion, press `Tab`.

Alternatively, go to Code | Code Completion | Insert Inline Proposal in the main menu or configure a different shortcut.

  * To accept a suggestion word by word, press `Ctrl+Right` or go to Code | Code Completion | Insert Inline Proposal's Word in the main menu.

  * To accept a suggestion line by line, press `End` or go to Code | Code Completion | Insert Inline Proposal's Line in the main menu.




### Type Info and Quick Documentation

If you want more information about a symbol at caret, for example, where it comes from or what its type is, the [Quick Documentation](viewing-reference-information.html#inline-quick-documentation) is your friend. Press `Ctrl+Q` to invoke it, and you will see a popup with these details.

If you do not need the full info, then use the Type Info action instead: place the caret at a code element and press `Ctrl+Shift+P` or go to View | Type Info in the main menu. It only shows the type of the selected expression but does not take up that much of screen space.

![Showing the expression type info](https://resources.jetbrains.com/help/img/idea/2025.3/type-info.png)

### Code completion case sensitivity

By default, IntelliJ IDEA code completion case sensitivity only affects the first letter you type. This strategy can be changed in the Settings dialog (`Ctrl+Alt+S`) on the Editor | General | Code Completion page, where you can make the IDE sensitive to all letters.

![Code Completion settings](https://resources.jetbrains.com/help/img/idea/2025.3/code_completion.png)

Here, you can also turn off the Show suggestions as you type option. This makes sense if you want the code completion popup to show up only when you explicitly call it.

### CamelHumps

By default, when you select anything in the editor, IntelliJ IDEA is not sensitive to the case of the words. If you prefer to select words according to CamelCase, for example, instead of selecting the whole word, select a part of it. You can enable this in Editor | General | Smart Keys of the Settings dialog.
