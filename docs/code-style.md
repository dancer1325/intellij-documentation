[//]: # (Source: https://www.jetbrains.com/help/idea/code-style.html)
[//]: # (Downloaded: 2025-12-17 19:20:50)

# Code style and formatting

If a company has certain coding guidelines, you have to follow them when creating source code. IntelliJ IDEA helps you maintain the required code style by formatting your code for you according to the code style rules.

IntelliJ IDEA offers two ways of defining code style rules.

You can use code style schemes: groups of settings that you can configure using the IDE interface, export, and share with other members of your team. Schemes are especially useful when you need to change the default code style settings for several projects at once.

For more information, refer to [Code style schemes](configuring-code-style.html).

The IDE also supports [EditorConfig](https://editorconfig.org/). If you have several code styles in your project (for example, for tests and for production code), you can have several .editorconfig files in corresponding folders in your project. This allows you to follow multiple code style standards at the same time.

For more information, refer to [EditorConfig](editorconfig.html).

Once the rules are configured, you can invoke the [Reformat code](reformat-and-rearrange-code.html) action that changes the formatting of your code in the selected code fragment, within a file, or across your entire project. Moreover, if you paste an unformatted piece of code to the editor, the IDE automatically reformats following the code style rules.

11 February 2024

[Multiple cursors and selection ranges](multicursor.html)[Code style schemes](configuring-code-style.html)
