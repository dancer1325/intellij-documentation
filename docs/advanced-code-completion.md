[//]: # (Source: https://www.jetbrains.com/help/idea/advanced-code-completion.html)
[//]: # (Downloaded: 2025-12-17 19:17:56)

## Type-matching completion

Smart type-matching code completion filters the suggestion list and shows only the types applicable to the current context.

Type-matching completion is useful in situations when it is possible to determine the appropriate type:

  * In the right part of assignment statements

  * In variable initializers

  * In `return` statements

  * In the list of arguments of a method call

  * After the `new` keyword in an object declaration

  * In chained expressions




### Invoke type-matching completion

  1. To invoke type-matching completion, start typing and press `Ctrl+Shift+Space` or select Code | Code Completion | Type-Matching from the main menu. 

![Smart code completion](https://resources.jetbrains.com/help/img/idea/2025.3/smartTypeCompletion.png)
  2. If necessary, press `Ctrl+Shift+Space` once again. This lets you complete: 

     * Collections, lists and arrays. IntelliJ IDEA searches for symbols with the same component type and suggests converting them.

     * Static method calls or constant references. IntelliJ IDEA scans for static methods and fields and suggests the ones suitable in the current context.

![smart type completion second call](https://resources.jetbrains.com/help/img/idea/2025.3/SmartTypeCompletionSecondCall.png)



Completion for chained expressions is only available for Java and requires the project to be built with the IntelliJ IDEA compiler (not the Gradle compiler).
