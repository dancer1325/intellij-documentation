[//]: # (Source: https://www.jetbrains.com/help/idea/extract-class-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:26:12)

# Extract Class Dialog

Use this page to specify the settings for the extract delegate refactoring.

Item| Description  
---|---  
Name for new class| Specify the name of the class to be created. If you want to define a class within the existing one, select the Create nested class option.  
Package name| Specify the name of the destination package for the new class.   
Target destination directory| Specify the directory for the class you are defining.  
Members to extract| Select the fields and methods to be extracted to the new class. IntelliJ IDEA can also generate getters if you select the Generate accessors option.  
Visibility| Select the visibility level for the members you are extracting. You can select from the following options:

  * Escalate: this option is selected by default and means that the visibility of extracted members will change to ensure that the current calls to the delegated elements can be compiled.
  * As is: select this option if you want to use the existing visibility for the members you are extracting.
  * Private: select this option to make the extracted members private.
  * Package local: select this option to make the extracted members belong to only the local package.
  * Protected: select this option to make the extracted member protected.
  * Public: select this option to make all of the extracted members public.

  
  
11 February 2024

[Extract Constant dialog](extract-constant-refactoring-dialog.html)[Extract Field Dialog](extract-field-dialog.html)
