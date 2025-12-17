[//]: # (Source: https://www.jetbrains.com/help/idea/command-completion.html)
[//]: # (Downloaded: 2025-12-17 19:21:02)

# Command completion

Command completion helps you write and transform code by suggesting context-aware IDE actions in the editor. It serves as a universal entry point, reducing the need to memorize shortcuts or search through menus. By providing suggestions that fit the current context, command completion helps you focus on your tasks and maintain a smooth coding flow.

Unlike [basic code completion](auto-completing-code.html), which suggests identifiers or keywords, command completion focuses on completing ideas. It prompts you to modify your code by applying context-aware actions. Depending on where you are in your code, the completion suggestions may include:

  * Fixes for issues: [intention actions and quick-fixes](intention-actions.html) available directly from the completion popup.

  * Code transformations: actions for [reformatting code](reformat-and-rearrange-code.html), [introducing variables](extract-variable.html), and other structural changes.

  * Refactoring and navigation: commonly used actions such as [renaming](rename-refactorings.html) or [navigating to a declaration](navigating-through-the-source-code.html#go_to_declaration), as well as context-specific ones like [changing a signature](change-signature.html).

  * Code generation: actions to generate [constructors](generating-code.html#generate-constructors), [getters and setters](generating-code.html#generate-getters-setters), [`toString()`](generating-code.html#generate-tostring), and more.

  * Framework-specific suggestions: when working with frameworks like Spring, IntelliJ IDEA may suggest relevant actions, for example, Spring bean wiring.




When used on code blocks, command completion can also suggest high-level transformations, such as [extracting the block into a method](extract-method.html) (currently, available for loops and `if` statements) or wrapping it in a control-flow statement.

### Toggle command completion on and off

Command completion is enabled in IntelliJ IDEA by default.

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | General | Code Completion.

  2. Use the Enable command completion option to enable or disable the feature.




### Invoke command completion

  * Start typing your code. Whenever you want to access the list of commands, type two dots (`..`).

![Command completion suggestions](https://resources.jetbrains.com/help/img/idea/2025.3/ij_command_completion.png)
  * Type one dot (`.`) to see command completion options together with the regular completion.

To make command completion suggestions easier to distinguish, IntelliJ IDEA displays them in a separate group. You can enable or disable grouping using the Show command completion as a separate group option in Settings | Editor | General | Code Completion.




To search through the list of command suggestions, type the option you are looking for. IntelliJ IDEA automatically displays the preview of the change when you select a command in the list.

![Search in command completion](https://resources.jetbrains.com/help/img/idea/2025.3/command_completion_search.png)

### Use command completion in read-only files

In read-only files, such as external library sources, you can use command completion to quickly find actions that help you [navigate your codebase](navigating-through-the-source-code.html#navigate_between_code_elements), [search for usages](find-highlight-usages.html), or [copy references](working-with-source-code.html#copy_paste).

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | General | Code Completion.

  2. Select the Enable command completion for read-only files option to enable the feature.

  3. Open a read-only file in the editor. Place the caret at the end of a symbol and type one dot (`.`) to access the list of available commands.

![Command completion in read-only files](https://resources.jetbrains.com/help/img/idea/2025.3/command_completion_read_only.png)
  4. Start typing the name of the action you are looking for, select it from the list, and press `Enter` to invoke it.




11 November 2025

[Advanced completion](advanced-code-completion.html)[Postfix completion](postfix-code-completion.html)
