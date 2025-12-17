[//]: # (Source: https://www.jetbrains.com/help/idea/extract-superclass-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:26:34)

# Extract Superclass Dialog

Refactor | Extract Superclass

Item| Description  
---|---  
Extract superclass from| This read-only field shows the name of the source package that contains the class to extract a superclass from.  
Extract superclass| When this option is selected, IntelliJ IDEA extracts a new superclass but does not use it immediately and the source code is not changed.  
Superclass name| In this field, type the name for the new superclass. The field is available if the Extract superclass option is selected.  
Extract superclass and use it where possible| Select this option to have a superclass extracted and immediately applied to the source code, with the suggested changes displayed in the dedicated tab of the [Find](find-tool-window.html) tool window.  
Rename original class and use superclass where possible| Use this option to rename the original class and make it an implementation of the newly created superclass.  
Rename original class to| In this field, type the new name for the original class. The field is available if the Rename original class and use superclass where possible option is selected.  
Package for new superclass| In this list, specify the package for the new superclass. If necessary, click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and choose the target package in the dialog that opens.  
Members to Form Superclass| In this area, specify the members of the class to be moved or delegated to the new superclass. To have an element included in the interface, select the checkbox next to it.  
Make Abstract| Select this option to leave the method implementation within the current class, and declare it abstract in the extracted superclass.  
JavaDoc/ASDoc for abstracts| In the JavaDoc /ASDoc area, specify the action to be applied to the inline documentation. The available options are: 

  * As is \- select this option to have the inline documentation left where it is.
  * Copy \- select this option to have the inline documentation copied to the extracted superclass without removing it from its current location.
  * Move \- select this option to have the inline documentation moved to the extracted superclass and delete it from its current location.

  
  
08 October 2024

[Extract Parameter Object Dialog](extract-parameter-object-dialog.html)[Extract Variable dialog](extract-variable-refactoring-dialog.html)
