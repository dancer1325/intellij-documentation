[//]: # (Source: https://www.jetbrains.com/help/idea/code-style-kotlin.html)
[//]: # (Downloaded: 2025-12-17 19:20:30)

## Tabs and Indents

Item| Description  
---|---  
Use tab character| Use the `Tab` key for indentation. When the checkbox is cleared, IntelliJ IDEA uses spaces instead of tabs.   
Smart tabs| 

  * If this checkbox is selected, the indentation for nested code blocks will use tabs and spaces as needed, while alignment indentation will use only spaces.
  * If this checkbox is cleared, only tabs are used. This means that a group of spaces that fits the specified tab size is automatically replaced with a tab, which may result in breaking fine alignment.

The Smart tabs checkbox is available if the Use tab character option is enabled.   
Tab size| In this field, specify the number of spaces included in a tab.  
Indent| In this field, specify the number of spaces to be inserted for each indent level.   
Continuation indent| Specify the indentation for lines that continue from the previous line, making it clear that they are part of the same statement or block of code. Continuation indents are used when a single statement is too long to fit on one line.  
Keep indents on empty lines| If this checkbox is selected, IntelliJ IDEA will keep indents on the empty lines as if they contained some code.If this checkbox is cleared, IntelliJ IDEA will delete the tab characters and spaces.
