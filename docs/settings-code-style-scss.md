[//]: # (Source: https://www.jetbrains.com/help/idea/settings-code-style-scss.html)
[//]: # (Downloaded: 2025-12-17 20:00:41)

## Tabs and Indents

Use tab character| 

  * If this checkbox is selected, tab characters are used:
    * On pressing the `Tab` key
    * For indentation
    * For reformatting code
  * If the checkbox is cleared, IntelliJ IDEA uses spaces instead of tabs.

  
---|---  
Smart tabs| An indentation consists of two parts. One part results from nesting code blocks, and the other part is determined by alignment.

  * If this checkbox is selected, the part that results from nesting contains both tabs and spaces (if necessary), while the part defined by alignment consists only of spaces.
  * If this checkbox is cleared, only tabs are used. This means that after reformatting a group of spaces that fits the specified tab size is automatically replaced with a tab, which may result in breaking fine alignment.

The Smart Tabs checkbox is available if the Use tab character checkbox is selected.  
Tab size| In this field, specify the number of spaces that fits in a tab.  
Indent| In this field, specify the number of spaces to be inserted for each indent level.  
Continuation indent| In this field, specify the number of spaces to be inserted between the values of properties.  
Keep indents on empty lines| If this checkbox is selected, IntelliJ IDEA retains indents on empty lines as if they contained some code. If the checkbox is cleared, IntelliJ IDEA deletes the tab characters and spaces on empty lines.
