[//]: # (Source: https://www.jetbrains.com/help/idea/extract-field-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:26:17)

# Extract Field Dialog

Item| Description  
---|---  
Field of type/Name| In this field, specify the name of the new field.  
Initialize in| In this area select where the new field will be initialized in.  
Visibility| In this area, specify the _visibility scope_ for the new field. The available options are:

  * Public \- if you select this option, the new field will be accessible from anywhere.
  * Private \- if you select this option, the new field will be accessible only from the current class.
  * Protected \- if you select this option, the new field will be accessible from the current class as well as from its inherited and parent classes.
  * Package local \- if you select this option, the new field will be accessible from the classes of the current package only.

  
Replace all occurrences| Select this checkbox to have IntelliJ IDEA automatically replace all the occurrences of the selected expression.The checkbox is enabled only if the selected expression is used more than once in the class. All the found occurrences of the expression are highlighted.  
Declare final| Check this option to create a final field.  
Delete variable declaration| Check this option to delete variable declaration.  
  
08 October 2024

[Extract Class Dialog](extract-class-dialog.html)[Extract Include File Dialog](extract-include-file-dialog.html)
