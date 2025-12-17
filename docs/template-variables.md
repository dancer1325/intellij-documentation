[//]: # (Source: https://www.jetbrains.com/help/idea/template-variables.html)
[//]: # (Downloaded: 2025-12-17 20:04:05)

## Predefined template variables

IntelliJ IDEA supports the following predefined live template variables that cannot be modified:

  * `$END$` indicates the position of the caret when the code snippet is complete, and you can no longer press `Tab` to jump to the next variable.

  * `$SELECTION$` is used in surround templates and denotes the code fragment to be wrapped. After the template expands, it wraps the selected text as specified in the template. For example, if you select `EXAMPLE` in your code and invoke the `"$SELECTION$"` template via the assigned abbreviation or by pressing `Ctrl+Alt+T` and selecting the desired template from the list, IntelliJ IDEA will wrap the selection in double quotes as follows: `"EXAMPLE"`.



