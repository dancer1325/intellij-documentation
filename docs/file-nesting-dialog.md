[//]: # (Source: https://www.jetbrains.com/help/idea/file-nesting-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:26:51)

# File nesting rules

You can configure the presentation of files with the same names but with different suffixes. Such file bunches can be presented as plain structures or the parent files can be shown as folders (nests) with their child files inside.

Such bunches of files may appear in framework-specific projects, for example, if you use [Angular](https://angular.io/).

![File nesting rules applied vs file nesting rules not applied](https://resources.jetbrains.com/help/img/idea/2025.3/nesting-rules-on-off.png)

### Configure file nesting

  1. In the Project tool window (`Alt+1`), click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moreVertical.svg) and select Appearance, then select File Nesting.

A dialog opens in which you can configure file nesting rules.

  2. Enable the Show files with the same names as nested option to recognize child files based on the patterns from the list and display them grouped under the corresponding parents.

Otherwise, IntelliJ IDEA shows parents and children at the same level.

  3. Configure nesting rules. You can edit predefined rules or specify new ones: click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and specify suffixes of parent and child files.

![the File Nesting dialog](https://resources.jetbrains.com/help/img/idea/2025.3/file-nesting-dialog.png)

When configuring a rule, consider the following:

     * Multilevel nesting is not supported. For example, if a TypeScript file file.ts is compiled into file.js with file.js.map generated, both file.js and file.js.map are shown right under file.ts.

     * Wildcards are not welcome.

  4. Click OK.




Nesting rules apply only to the files with the same names within the same directory.

If the names of two files match a pattern but the files are stored in different directories, IntelliJ IDEA does not visually "move" any of them.

10 February 2025

[Project tool window](project-tool-window.html)[Modules](creating-and-managing-modules.html)
