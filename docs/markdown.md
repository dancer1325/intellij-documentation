[//]: # (Source: https://www.jetbrains.com/help/idea/markdown.html)
[//]: # (Downloaded: 2025-12-17 19:32:01)

## Code blocks

To insert a fenced code block, use triple backticks ````` before and after the code block. If you specify the language for the code block, by default, the Markdown editor [injects the corresponding language](using-language-injections.html).

This enables syntax highlighting and other coding assistance features for the specified language: [completion](auto-completing-code.html), [inspections](code-inspection.html), and [intention actions](intention-actions.html).

![Insert a fenced code block in Markdown](https://resources.jetbrains.com/help/img/idea/2025.3/markdown-code-blocks.png)

### Disable coding assistance in code blocks

If your code blocks are not meant to be syntactically correct, you may want to disable code injection and syntax errors in code blocks.

  1. Press `Ctrl+Alt+S` to open settings and then select Languages & Frameworks | Markdown.

  2. Clear the following options:

     * Inject languages in code fences

     * Show problems in code fences

  3. Click OK to apply the changes.




### Run commands from Markdown files

When you clone a project, there is usually a README.md file with instructions and commands to run the application, configure your environment, and so on. IntelliJ IDEA detects these commands and provides gutter icons for running the commands.

  * Click the corresponding gutter icon or press `Ctrl+Shift+F10` while the caret is at the command that you want to run.

![Gutter icons for running commands detected in Markdown files](https://resources.jetbrains.com/help/img/idea/2025.3/markdown-run-code-block-gutter-icon.png)



You can disable the gutter icons for running commands in Markdown files in IDE settings `Ctrl+Alt+S` under Languages & Frameworks | Markdown: clear the Detect commands that can be run right from Markdown files checkbox.

For more information, refer to [Markdown language settings](markdown-reference.html).
