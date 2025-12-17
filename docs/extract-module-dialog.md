[//]: # (Source: https://www.jetbrains.com/help/idea/extract-module-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:26:30)

# Extract Module Dialog

Refactor | Extract Module

Item| Description  
---|---  
Extract module from| This read-only field displays the name of Ruby class, from which a module should be extracted.  
Module name| In this text field, type the name of the target module. The module name should a proper Ruby constant.  
Directory for new module| In this text field, specify the path to the target directory, where the new module will be stored. Use code completion while you type the path:![ruby_ExtractModule3.png](https://resources.jetbrains.com/help/img/idea/2025.3/ruby_ExtractModule3.png)You can also click the ellipsis button, or press `Shift+Enter`, and select the desired path in the Select Path dialog.  
Context to form module| Click one of the radio buttons (Instance or Static) to define the way the new module will be used in a Ruby class.  
Members to form module| This area displays the list of members detected in the original class. Select the checkboxes next to the members to be included in the new module. Note that static methods are disabled when Instance context is selected, and vice versa.  
  
11 February 2024

[Extract Method Object Dialog](extract-method-object-dialog.html)[Extract Parameter Object Dialog](extract-parameter-object-dialog.html)
