[//]: # (Source: https://www.jetbrains.com/help/idea/change-signature-for-scala.html)
[//]: # (Downloaded: 2025-12-17 19:19:46)

# Change Signature for Scala

Use this dialog to perform the [Change Signature refactoring](change-signature.html).

Use the available controls to make changes to the method signature. Specify how the method calls should be handled.

Click Refactor to perform the refactoring right away. Click Preview to see the potential changes in the [Find tool window](find-tool-window.html) prior to the actual refactoring.

Item| Description  
---|---  
Visibility| Select the method visibility scope (access level modifier) from the list.  
Return type| Use this field to modify the method return type.[Code completion](auto-completing-code.html) `Ctrl+Space` is available in this field, and also in other fields used for specifying the types.  
Name| Use this field to modify the method name.  
Modify method calls| The existing method calls are modified so that the method with the new signature is called.  
Add to definition| If this option is selected, new parameters are added to a method definition.  
Specify result type| Use this option to configure type annotation settings.  
Signature Preview| In this area, the current method signature is shown. (The information in this area is synchronized with the changes you are making to the method signature.)  
  
In the area where parameters are specified, you can add new ones, edit, reorder or delete the existing ones. The refactoring will distribute your changes accordingly.

To start editing a parameter, click it. Alternatively, use the `Up` and `Down` arrow keys to navigate to the parameter of interest and `Enter` to start modifying it.

Item| Tooltip and shortcut| Description  
---|---|---  
![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)| Add`Alt+Insert`| Add a new parameter.Specify the parameter information in the corresponding fields. (The default parameter value is the value (or the expression) to be passed to the method in the method calls.)  
![the Remove button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)| Remove`Alt+Delete`| Delete the selected parameter.  
![the Up button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moveUp.svg)| Up`Alt+Up`| Move the selected parameter one line up in the list of parameters.  
![the Down button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moveDown.svg)| Down`Alt+Down`| Move the selected parameter one line down in the list of parameters.  
  
11 February 2024

[Change Class Signature dialog](change-class-signature-dialog.html)[Convert anonymous to inner](convert-anonymous-to-inner.html)
