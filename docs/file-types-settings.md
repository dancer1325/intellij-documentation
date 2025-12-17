[//]: # (Source: https://www.jetbrains.com/help/idea/file-types-settings.html)
[//]: # (Downloaded: 2025-12-17 19:26:54)

# File Types

This page describes controls. For more information about configuring a copyright notice, refer to [Copyright](copyright.html).

This page describes controls. For more information about configuring a copyright notice, refer to [Copyright](copyright.html).

Item| Description  
---|---  
No copyright| If this option is selected, the copyright notice will not be updated in the files of the selected type.  
Use default settings| If this option is selected, the copyright notice will be updated according to the [default settings for new projects](configure-project-settings.html#new-default-settings).  
Use custom formatting options| If this option is selected, the copyright notice in the files of the selected type will be updated according to the custom settings defined below.  
Comment Type| In this area, specify the type of comment to enclose copyright notices in. The available options are:

  * Use block comment: select this option to have copyright notices enclosed in block comments.
  * Prefix each line: select this checkbox to have each line of a copyright notice prepended with the character defined in the Separator field. By default, an asterisk is used.
  * Use line comment: select this option to have copyright notices represented as a sequence of line comments.

  
Borders| In this area, define how to separate copyright notices from other comments.

  * Separator before: select this checkbox have a copyright notice prepended with a line of characters defined in the Separator field.
  * Separator after: select this checkbox have a copyright notice followed by a line of characters defined in the Separator field.
  * Separator: in this field, type the character that will be used in the separator strings and as a prefix or ending character in block comments.
  * Length: in this field, type the number of characters in a separator line.
  * Box: select this checkbox to have each line of a copyright notice followed by a character defined in the Separator field.
  * Add blank line before: select this checkbox to have a blank line inserted before a copyright notice.
  * Add blank line after: select this checkbox to have a blank line inserted after a copyright notice.

  
Relative Location| In this area, specify the location of a copyright notice relative to other comments.

  * Before other comments: when this option is selected, copyright notices are inserted above other comments.
  * After other comments: when this option is selected, copyright notices are inserted below other comments.

  
Preview| Use this area to view a sample copyright notice with the formatting you have defined.  
Location in File| Use this area to specify the location of the copyright notice in a file. Depending on the file type, the available options are:

  * JAVA
    * Before the package statements
    * Before imports
    * Before the class declaration
  * HTML, JSP, JSPX, XML
    * Before the root tag
    * Before the Doctype statement
  * For Properties, PHP, JavaScript, CSS, SCSS, and SASS file types no choice is available. Copyright notices are always inserted at the top of a file.

  
  
11 October 2024

[Formatting](formatting.html)[Emmet](settings-emmet.html)
