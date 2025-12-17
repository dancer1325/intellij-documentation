[//]: # (Source: https://www.jetbrains.com/help/idea/coding-assistance-in-groovy.html)
[//]: # (Downloaded: 2025-12-17 19:20:57)

## Code completion

When you access [Basic Completion](auto-completing-code.html) by pressing `Ctrl+Space`, you get basic suggestions for variables, types, methods, expressions, for a parameter name you get type suggestions and so on. When you call Basic Completion twice, it shows you more results.

The [Smart Completion](advanced-code-completion.html#smart_type_matching_completion) feature is aware of the expected type and data flow, and offers the options relevant to the context. To call Smart Completion, press `Ctrl+Shift+Space`. When you call Smart Completion twice, it shows you more results, including chains.

![Code completion](https://resources.jetbrains.com/help/img/idea/2025.3/groovy_code_completion_import.png)

To overwrite the identifier at the caret, instead of just inserting the suggestion, press `Tab`. This is helpful if you're editing part of an identifier, such as a filename.

To let IntelliJ IDEA complete a statement for you, press `Ctrl+Shift+Enter`. [Statement Completion](advanced-code-completion.html#statements_completion) will automatically add the missing parentheses, brackets, braces and the necessary formatting.

The [Postfix Completion](postfix-code-completion.html) feature lets you transform an already typed expression to another one, based on the postfix you type after a dot.

For more information, refer to [Auto-Completing Code](auto-completing-code.html).
