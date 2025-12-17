[//]: # (Source: https://www.jetbrains.com/help/idea/move-class-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:32:40)

# Move Class Dialog

The Move Class refactoring dialog is invoked for the classes selected in the Project view, or opened in the editor.

Item| Description  
---|---  
To package| Specify the destination package. Click the ellipsis button, and select the target package in the Choose Destination Package dialog that shows a tree view of all packages within the project. The content of a package is moved along with the package from the old location to the new destination package.  
Make inner class of| If you want to make your class inner, specify the target class. Click the ellipsis button and select the target class in the Choose Class dialog.   
Search in comments and strings| Select this option to apply the changes to comments and strings.  
Search for text occurrences| Select this option to apply the changes to documentation, HTML, JSP, and other non-Java files included in your project.  
Search for references| Select this checkbox to have the changes applied to the references. This option is available only for Move File or Move Package refactorings.  
Move to another source folder| If this option is selected, you can select the target root, where the destination package will be located. If the option is not selected, only the current root is used. This option is disabled for the modules that contain a single source root.  
Target destination directory| When the dialog opens, the field shows the path to the folder where the file that implements the class to move is currently stored. The path is displayed in the following format: ...\<project root>\<current namespace folder relative to the project root> The path is updated automatically as you specify the namespace to move the class to. However, if you are going to move a class to a non-existing namespace under another parent namespace, IntelliJ IDEA will not suggest the proper folder unless you appoint a root folder for your namespace structure by marking the relevant folder as Sources on the Directories page of the Settings dialog (`Ctrl+Alt+S`) . Do one of the following:

  * Accept the preselected path displayed in the field.
  * Choose another path from the list. All of them are evaluated from the namespace root or from the current directory, so it is safe to choose any of them.
  * Click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.open.svg) and select a folder in the dialog that opens.
  * Press `F2` and edit the preselected path. Keep in mind that this may cause problems with automatic loading in the future.

  
Open in editor| Select this checkbox to open the moved class in the editor.  
  
10 September 2024

[Move dialogs](move-dialogs.html)[Move Directory dialog](move-directory-dialog.html)
