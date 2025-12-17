[//]: # (Source: https://www.jetbrains.com/help/idea/extract-constant-refactoring-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:26:14)

# Extract Constant dialog

Use this dialog to configure options for the [Extract Constant](extract-constant.html) refactoring.

Item| Description  
---|---  
Constant of type| IntelliJ IDEA automatically determines the field type.  
Name| Specify here the name for the new constant.  
Introduce to class| Select the class in which the constant will be introduced.  
Introduce as enum constant| If you've selected an enum class in the Introduce to class field, you can use this option to select, whether you want to introduce this constant as an enum constant, or as a usual field. Otherwise, this option is naturally disabled and does not affect anything.  
Visibility| Select the visibility scope for the new field.  
Replace all occurrences| Check this option to automatically replace all the occurrences of the selected expression (if the selected expression is found more than once in the class).  
Delete variable declaration| Check this option to delete variable declaration.  
Annotate field as @NonNls| Check this option to avoid changes during localization.

  * This field is only available if the project is configured to use annotations, that is, the library annotation.jar is added to the project or module. If annotations are not available, this option does not appear in the dialog.
  * The project language level should be 5.0 to support annotations.

  
  
02 September 2025

[Extract dialogs](extract-dialogs.html)[Extract Class Dialog](extract-class-dialog.html)
