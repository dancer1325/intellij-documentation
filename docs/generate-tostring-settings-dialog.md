[//]: # (Source: https://www.jetbrains.com/help/idea/generate-tostring-settings-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:27:36)

## Settings tab

Item| Description  
---|---  
Use fully qualified class name in code generation ($classname)| If this checkbox is selected, the dumped classnames will include their package names. (The `$classname` variable in the [Velocity templates](#templates))  
Enable getters in code generation ($method)| If this checkbox is selected, the code generator will have `$methods` variable in the Velocity Macro Language.See [example 2](generating-code.html#generate-tostring).  
Move caret to the generated method| If this checkbox is selected, the caret scrolls to the generated `toString()` method.  
Sort elements| If this checkbox is selected, the members are sorted in the selected order (ascending or descending).  
When method already exists| In this section, choose the default conflict resolution policy: 

  * Ask: Choose this option to ask for confirmation, if a `toString()` method already exists. IntelliJ IDEA shows the dialog Replace existing toString method.The answer Yes results in generating the new `toString()` method in place of the existing one; the answer No results in creating a duplicate method.
  * Replace existing: Choose this option to automatically replace the existing `toString()` code.
  * Generate duplicating method: Choose this option to create a duplicate `toString()` method; in doing so, the new method will have the name `toString()`; the existing code will not be erased.

  
Where to insert?| In this section, choose the place to insert the generated `toString()` method. The possible options are: 

  * At caret.
  * After equals() and hashCode(): the generated `toString()` method will be inserted after the equals/hashCode, if present in the Java class; otherwise, the new method will be inserted at the current caret position.
  * At the end of class: the generated `toString()` method will be inserted as the last method.

  
Exclude| In this section, select the checkboxes next to the elements to be excluded from the `toString()` method generation: 

  * Exclude constant fields: If this checkbox is selected, then any constants won't be a part of the available fields for the code generator.
  * Exclude static fields: If this checkbox is selected, then any fields that have static modifiers won't be a part of the available fields for the code generator.
  * Exclude transient fields: If this checkbox is selected, then any fields with transient modifiers won't be a part of the available fields for the code generator.
  * Exclude enum fields: If this checkbox is selected, then any fields of the type `enum` (JDK1.5) won't be a part of the available fields for the code generator.
  * Exclude logger fields (Log4j, JDK Logging, Jakarta Common Logging): If this checkbox is selected, then any field that is either Log4j Logger, Java JDK Logger, or a Jakarta Commons Logger won't be a part of the available fields for the code generator.
  * Exclude fields by name (reg exp): If this checkbox is selected, then IntelliJ IDEA performs a regular expression matching on the field name. If the result is true, then the field won't be a part of the available fields for the code generator.
  * Exclude fields by type name (reg exp): If this checkbox is selected, then IntelliJ IDEA performs a regular expression matching on the field type name (fully qualified name). If the result is true, the field won't be a part of the available fields for the code generator.
  * Exclude methods by name (reg exp): If this checkbox is selected, then IntelliJ IDEA performs a regular expression matching on the method name. If the result is true, the method won't be a part of the available methods for the code generator.
  * Exclude methods by return type name (reg exp): If this checkbox is selected, then IntelliJ IDEA performs a regular expression matching on the method return type name (fully qualified name). If the result is true, the method won't be a part of the available methods for the code generator.


