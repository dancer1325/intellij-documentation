[//]: # (Source: https://www.jetbrains.com/help/idea/extract-method-dialog-for-groovy.html)
[//]: # (Downloaded: 2025-12-17 19:26:25)

# Extract Method Dialog for Groovy

Refactor | Extract Method `Ctrl+Alt+M`

Item| Description  
---|---  
Visibility| In this area, specify the visibility scope of the method to be generated.  
Name| In this field, specify the name of the function or method to be generated on the basis of the selected source code.  
Specify return type explicitly| This checkbox is available if you invoke refactoring from the method of a Groovy class. Select this checkbox to return a data type of the value explicitly.  
Use explicit return statement| This checkbox is active if the method returns a value. You can omit `return` keyword if it is the last return statement in the method. If you select this checkbox the keyword is returned.  
Parameters| In this area, select parameters to be passed to the new method/function. If a parameter that is critical for the functionality of the new method is not selected, IntelliJ IDEA will be unable to proceed with the refactoring.  
Move Up/Down| Use these buttons to change the order of the parameters.  
Signature preview| In this read-only field, view the declaration of the new method/function.  
  
11 February 2024

[Extract Method dialog](extract-method-dialog.html)[Extract Method Object Dialog](extract-method-object-dialog.html)
