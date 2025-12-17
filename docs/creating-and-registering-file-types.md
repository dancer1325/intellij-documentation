[//]: # (Source: https://www.jetbrains.com/help/idea/creating-and-registering-file-types.html)
[//]: # (Downloaded: 2025-12-17 19:23:22)

## Add a custom file type

If you work on a language that is not supported by default and there are no [plugins](https://plugins.jetbrains.com/idea) for it, you can configure a simple language service for files associated with this language — you will enjoy syntax highlighting for keywords, comments, and braces and have some basic editor helpers such as adding line/block comments with `Ctrl+/`/`Ctrl+Shift+/` and extending/shrinking selection according to the structure with `Ctrl+W`/`Ctrl+Shift+W`.

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | File Types.

  2. In the Recognized File Types section, click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg), specify the name of the new type, and provide a description.

  3. In the Syntax Highlighting section, configure case sensitivity, brace matching settings, and specify ways of defining comments:

     * Line comment: specify characters that indicate the beginning of a single-line comment.

     * Only at line start: characters that indicate the beginning of a line comment are recognized as a comment if they are located at the beginning of a line.

     * Block comment start, Block comment end: specify characters that indicate the beginning and the end of a block comment.

     * Hex prefix: specify characters that indicate that the subsequent value is a hexadecimal number (for example, `0x`).

     * Number postfixes: specify characters that indicate which numeric system or unit is used. A postfix is a trailing string of characters (for example, `e-3, kg`).

     * Support paired braces, Support paired brackets, Support paired parens, Support string escapes: select these checkboxes to highlight paired braces, brackets, parentheses, and string escapes.

  4. In the Keywords section, you can specify up to four lists of keywords. Keywords of each list will be highlighted differently in the editor and will be auto-completed.

  5. The Ignore case checkbox indicates whether keywords in files of the custom format are case-sensitive.

![Creating a new file type](https://resources.jetbrains.com/help/img/idea/2025.3/custom-file-type.png)
  6. You can customize colors for syntax highlighting of language-specific keywords, comments, and other identifiers on the Editor | Color Scheme | User-Defined File Types settings page.




In IntelliJ IDEA, recognized files are not always supplied with extensive support. For example, .php files are recognized in the [IntelliJ IDEA Community Edition](https://www.jetbrains.com/idea/features/editions_comparison_matrix.html) and marked with the corresponding icon, although this edition does not provide PHP development support.
