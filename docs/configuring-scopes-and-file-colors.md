[//]: # (Source: https://www.jetbrains.com/help/idea/configuring-scopes-and-file-colors.html)
[//]: # (Downloaded: 2025-12-17 19:22:02)

## Define a new scope

In IntelliJ IDEA, there's a set of [predefined scopes](#predefined-scopes-list), but you can also define your own scopes.

  1. Press `Ctrl+Alt+S` to open settings and then select Appearance & Behavior | Scopes.

  2. Click the Add Scope button (![the Add Scope button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg)) and select what kind of scope you want to define: [local](#local-sc) or [shared](#shared-sc).

You can change the state of the selected scope (local or shared) later using the Share through VCS checkbox.

![Creating a new scope: selecting between a shared and a local scope](https://resources.jetbrains.com/help/img/idea/2025.3/scopes-local-shared.png)
  3. In the dialog that opens, name the new scope and click OK.

  4. Add files to the new scope. Select the necessary items in the project tree and click one of the options located on the right from the tree:

     * Include: include the selected items. If you are including a folder, this action adds only the files located inside this folder. All nested subfolders and their contents will not be included.

     * Include Recursively: include the selected folder together with the nested subfolders and their contents.

     * Exclude: exclude the selected items from the scope. If you are excluding a folder, this action removes only the files located inside this folder. All nested subfolders and their contents will remain in the scope.

     * Exclude Recursively: exclude the selected folder together with the nested subfolders and their contents.

![A new scope with added files and folders](https://resources.jetbrains.com/help/img/idea/2025.3/scope-created.png)

As you add files to the scope, IntelliJ IDEA creates an expression and displays it in the Pattern field.

Instead of using the buttons, you can also type a pattern in the Pattern field manually using the [scope language syntax](scope-language-syntax-reference.html) reference.

  5. Apply the changes and close the dialog.




Files and folders displayed for the selected scope are shown in different colors to help you understand what is included and what is not:

  * ![the green color sample](https://resources.jetbrains.com/help/img/idea/2025.3/green_square.png) Files and folders included in the scope.

  * ![the dark blue color sample](https://resources.jetbrains.com/help/img/idea/2025.3/blue_square.png) Folders that contain both excluded and included files and folders.

  * ![the black color sample](https://resources.jetbrains.com/help/img/idea/2025.3/black_square.png) Files and folders that are excluded from the selected scope.




After you create a custom scope, you can find it in the Project tool window and in [all dialogs](#features) that allow you to limit the number of files to which you want to apply an action.

![The new scope shown in the Project tool window](https://resources.jetbrains.com/help/img/idea/2025.3/scope-project-tw.png)
