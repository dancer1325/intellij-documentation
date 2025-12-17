[//]: # (Source: https://www.jetbrains.com/help/idea/move-namespace-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:32:48)

# Move Namespace Dialog

The dialog is available only if the PHP plugin is installed and enabled. The PHP plugin is not bundled with IntelliJ IDEA, but it can be installed on the Settings | Plugins page, tab Marketplace, as described in [Installing plugins from JetBrains Marketplace](managing-plugins.html#install_plugin_from_repo). 

The dialog opens when you select a PHP namespace to be moved and select Refactor | Move from the main menu or from the context menu of the selection.

IntelliJ IDEA assumes that the namespaces in your project are arranged in compliance with the [PSR-0/PSR-4 standard](https://www.php-fig.org/psr/psr-4/) and enforces you to retain the folder structure and the namespace hierarchy in accordance with this standard when moving namespaces.

When you specify a namespace to move a namespace to, IntelliJ IDEA automatically updates the Target Destination Directory field, which shows the path to the folder that corresponds to the namespace in question.

Item| Description  
---|---  
New Namespace Name| When the dialog opens, the field shows the fully qualified name of the selected namespace. Specify the new namespace name. Use only backslashes `\` as namespace separators.   
Target Destination Directory| When the dialog opens, the field shows the path to the folder corresponding to the current namespace. The path is displayed in the following format: ...\<project root>\<current namespace folder relative to the project root> The path is updated automatically as you specify the new namespace name. However, if you are going to move a namespace to another parent namespace, IntelliJ IDEA will not suggest the proper folder unless you appoint a root folder for your namespace structure by marking the relevant folder as Sources on the Directories page of the Settings dialog (`Ctrl+Alt+S`) . Do one of the following:

  * Accept the preselected path displayed in the field.
  * Choose another path from the list. All of them are evaluated from the namespace root or from the current directory, so it is safe to choose any of them.
  * Click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.open.svg) and select a folder in the dialog that opens.
  * Press `F2` and edit the preselected path. Keep in mind that this may cause problems with automatic loading in the future.

  
Refactor| Click this button to open the Move Files with Related Namespaces dialog and specify the classes and files to be moved to the new namespace and the new folder.The upper pane of the dialog lists the destination namespaces and folders for classes and files related to the namespace. Each item in the list corresponds to a class/file. When you move the caret to an item, the bottom pane shows the contents of the file related with it. ![ps_move_namespace_refactoring_move_files_dialog.png](https://resources.jetbrains.com/help/img/idea/2025.3/ps_move_namespace_refactoring_move_files_dialog.png)

  * To have a class and the corresponding file moved to the destination namespace and the destination folder, select the checkbox next to the namespace/folder. 
  * To add all the items to the list or remove all of them from the list, click Select All or Unselect All respectively. 

  
  
26 May 2024

[Move File dialog](move-file-dialog.html)[Rename dialogs](rename-dialogs.html)
