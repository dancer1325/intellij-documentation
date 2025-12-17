[//]: # (Source: https://www.jetbrains.com/help/idea/indentation.html)
[//]: # (Downloaded: 2025-12-17 19:29:24)

## Configure indentation style

In IntelliJ IDEA, you can configure indents in [code style schemes](configuring-code-style.html) or in [ .editorconfig](editorconfig.html) files.

To be able to use EditorConfig in your project, enable the [.editorconfig](editorconfig.html) plugin.

### Open indentation settings in the code style scheme

  1. Click the widget and select Configure Indents for <language_or_SQL_dialect>. 

![Configure Indents for Java](https://resources.jetbrains.com/help/img/idea/2025.3/configure-indents-for-java.png)
  2. In the dialog that opens, you can change settings for tabs and indents and also configure other code style settings. Click OK.

  3. [Reformat](reformat-and-rearrange-code.html) the necessary part of your project to apply new indentation settings.




### Open indentation settings in .editorconfig

Files in which code style settings are specified via [.editorconfig](editorconfig.html) files have the ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.ide.configFile.svg) icon in the widget.

  1. Click the widget and select Open .editorconfig.

The IDE opens the nearest .editorconfig file which affects the file that you're currently working with. To view a list of all available .editorconfig files, click Show Files Related to Project.

![EditorConfig menu opened from the Indentation widget](https://resources.jetbrains.com/help/img/idea/2025.3/editorconfig-widget-menu.png)
  2. Make your changes and [reformat](reformat-and-rearrange-code.html) the necessary part of your project to apply new indentation settings.




### Indentation settings for Java

Code style scheme settings are configured in Settings | Editor | Code Style | Java.

Code style setting| EditorConfig property| Description  
---|---|---  
Use tab character| `indent_style = tab``indent_style = space`| Use the tab or space character for indentation and code formatting.  
Smart tabs| `ij_smart_tabs = true``ij_smart_tabs = false`| When the option is on, the part of indentation defined by the nesting of code blocks is made of the tabs and (if necessary) spaces, while the part of indentation defined by the alignment is made only of spaces.When the option is off, a group of spaces that fits the specified tab size is automatically replaced with a tab, which may result in breaking fine alignment.  
Tab size| `tab_width`| The number of spaces that a tab should include.  
Continuation indent| `ij_continuation_indent_size`| Specify the indentation for lines that continue from the previous line, making it clear that they are part of the same statement or block of code. Continuation indents are used when a single statement is too long to fit on one line.  
Keep indents on empty lines| `ij_java_keep_indents_on_empty_lines`| Keep indents on the empty lines as if they contained some code. Otherwise, IntelliJ IDEA will delete the tab characters and spaces.  
Label indent| `ij_java_label_indent_size`| The number of spaces to be inserted at the next line before a label statement.  
Absolute label indent| `ij_java_label_indent_absolute`| Count label indentation as an absolute number of spaces. Otherwise, label indentation is counted relative to previous indent levels.  
Do not indent top level class members| `ij_java_do_not_indent_top_level_class_members`| Place top-level class members at the class declaration indentation level.  
Use indents relative to expression start| `ij_java_use_relative_indents`| Format blocks of code against the closest ancestor block that starts on a new line. Otherwise, blocks of code will be formatted in columns.
