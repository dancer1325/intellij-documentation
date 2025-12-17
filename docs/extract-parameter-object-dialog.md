[//]: # (Source: https://www.jetbrains.com/help/idea/extract-parameter-object-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:26:31)

# Extract Parameter Object Dialog

Refactor | Extract | Parameter Object

Use this refactoring to create a wrapper class around some selected parameters of a method, or use a compatible existing class as a wrapper.

Item| Description  
---|---  
Method to extract parameters from| This read-only field shows the name of the selected method.  
Parameter Class| Use this section to specify whether you want to create a new wrapper class or use an existing one.  
Create new class| Click this radio-button to move parameters of a method to a new class. If this option is selected, specify the class and destination package name in the fields below. By default, the current package name is displayed. You can type a different package name in the text field, or click the ellipsis button and select the destination package from the tree view. If the desired package doesn't exist, click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.newFolder.svg) to create a new one.  
Create inner class| Click this radio-button to move parameters of a method to an inner class. If this option is selected, specify the class name in the field below.  
Use existing class| Click this radio-button to move parameters of a method to an existing class of your choice. You can type the fully-qualified class name in the text field, or click the ellipsis button and choose the desired class in the Select parameter class dialog. Note that you can select the desired wrapper class both from the project and non-project classes.  
Parameters to extract| Use checkboxes in this section to select which parameters of a method should be extracted into a separate object.  
Move Up / Move Down| Use these buttons to move the selected reorder parameters in the list.  
Keep method as delegate| If this checkbox is selected, the original method will be preserved as a delegate to the newly created method.  
  
26 May 2024

[Extract Module Dialog](extract-module-dialog.html)[Extract Superclass Dialog](extract-superclass-dialog.html)
