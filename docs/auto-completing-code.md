[//]: # (Source: https://www.jetbrains.com/help/idea/auto-completing-code.html)
[//]: # (Downloaded: 2025-12-17 19:18:38)

## Exclude and prioritize classes for completion

### Exclude a class or package from completion

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | General | Auto Import.

  2. Under Exclude from import and completion, add the names of classes or packages that you want to exclude from completion. The classes you specify here will not appear in the suggestion list.




You can also exclude items from the completion list: press `Alt+Enter` when the list with completion suggestions is open and select the item you want to exclude.

### Prioritize classes for completion

This feature allows you to import frequently used static methods automatically. When you type a method from a prioritized class, the IDE shows completion suggestions. Selecting a suggestion from the list inserts the corresponding import statement without requiring manual edits.

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | General | Auto Import.

  2. In the Include auto-import of static members in completion section, click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) or press `Alt+Insert`.

  3. In the dialog that opens, specify the class you want to add to the list. You can search for the classes by name of select them from the project structure.

  4. To the right from the class name, you can also select whether you want to prioritize it in the current project only or in all projects (globally).



