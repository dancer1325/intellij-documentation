[//]: # (Source: https://www.jetbrains.com/help/idea/move-package-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:32:49)

# Move Package Dialog

Item| Description  
---|---  
Select refactoring| Specify which action you want to perform: [move package to another package](#toPackage), [move directory to another source root](#toSourceRoot), or [to another directory](#toDirectory).  
This dialog opens when Move package to another package option has been selected.  
To package| Specify the destination package. Click the ellipsis button, and select the target package in the Choose Destination Package dialog that shows a tree view of all packages within the project. The content of a package is moved along with the package from the old location to the new destination package.  
Search in comments and strings| Select this option to apply the changes to comments and strings.  
Search for text occurrences| Select this option to apply the changes to documentation, HTML, JSP, and other non-Java files included in your project.  
Search for references| Select this checkbox to have the changes applied to the references. This option is available only for Move File or Move Package refactorings.  
Move to another source folder| If this option is selected, you can select the target root, where the destination package will be located. If the option is not selected, only the current root is used. This option is disabled for the modules that contain a single source root.  
This dialog opens when Move directory to another source root option has been selected.  
Select source root| Choose the target source root from a tree view of source roots configured in your project.  
This dialog opens when Move directory to another directory option has been selected.  
To directory| Use this field to specify the destination directory. Click the ellipsis button, and select the target directory in the Select Path dialog.  
  
11 February 2024

[Move Directory dialog](move-directory-dialog.html)[Move Inner to Upper Level Dialog for Java](move-inner-to-upper-level-dialog-for-java.html)
