[//]: # (Source: https://www.jetbrains.com/help/idea/scala-features-overview-scala.html)
[//]: # (Downloaded: 2025-12-17 19:59:47)

## Working with Strings in Scala

IntelliJ IDEA with the Scala plugin, provides many tools to help with string manipulations in Scala programming This page highlights some of the most popular actions and shortcuts.

### Triple-quote strings

If you want to include a quote character (`'"'`) in a regular string, you need to escape it by writing a backslash in front of the character (`'\"'`). It is tedious if you have many quote characters in the string, and it may also lead to typos that are difficult to spot. Instead, you can convert your regular string into a triple-quote one. To do that, enter your string, press `Alt+Enter` and from the list of intentions, select Convert to """string""".

### Multi-line strings

With the same Convert to """string""" intention you can convert a regular string with escaped newline characters (`'\n'`) into a multi-line string. Press `Alt+Enter` to open the list of intentions. Select Convert to "string" and press `Enter`. You can use the same intention once again to revert it.

To enter a multi-line string from scratch, type triple quotes in the editor. If you press `Enter`, it will automatically invoke the `stripMargin` method. The `stripMargin` method removes the left part of a multi-line string up to a specified delimiter. The whitespaces are also preserved.

### Multi-line strings settings

Use the Multi-line strings tab in Scala settings to set a different format for multi-line string options such as Margin char indent or disable a multi-line strings support.

Press `Ctrl+Alt+S` to open settings and then select Editor | Code Style | Scala. Then, on the Scala page, select the Multi-line strings tab. Edit the settings and click OK.

![the Multi-line strings settings](https://resources.jetbrains.com/help/img/idea/2025.3/multi_line_strings.png)

Convert simple string into the interpolated one adding a variable reference.

### Concatenation with + +

An idiomatic Scala way to include computation results in strings is to use interpolation. If for some reason you decide to split your string into two and concatenate them with the computation result with '+' signs instead, move the cursor to the place where you want to have the string split, and from the list of intentions, select Insert gap with concatenation: (" + + ").

### The 'replace '\r'' intention

This intention lets you keep the caret at the correct place on the next line in the multi-line strings regardless of what operating system you have at the moment. Enter a multi-line string, press `Alt+Enter` and select the appropriate intention from the list.

![the replace intention](https://resources.jetbrains.com/help/img/idea/2025.3/add_replace_intention.png)

### Inject Language/Reference

Use the Inject Language/Reference intention to insert a language or a reference into your multi-line string literals. For more information, refer to [Language Injections](using-language-injections.html).

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Code Style | Scala.

  2. On the Scala page, select the Multi-line strings tab. 

![the Multi-line strings settings](https://resources.jetbrains.com/help/img/idea/2025.3/multi_line_strings.png)
  3. Edit the settings and click OK.



