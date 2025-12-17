[//]: # (Source: https://www.jetbrains.com/help/idea/code-style-vue.html)
[//]: # (Downloaded: 2025-12-17 19:20:47)

## Tabs and Indents

Specific to the language in the block| Select this option to have the contents of top-level tags indented in the language-specific style.  
---|---  
Same in the whole file| Select this option to apply uniform indentation to the code inside all top-level tags in a file. Use the controls below to configure uniform indentation.  
Use tab character| 

  * If this checkbox is selected, tab characters are used:
    * On pressing the `Tab` key
    * For indentation
    * For reformatting code
  * If the checkbox is cleared, IntelliJ IDEA uses spaces instead of tabs.

  
Smart tabs| An indentation consists of two parts. One part results from nesting code blocks, and the other part is determined by alignment.

  * If this checkbox is selected, the part that results from nesting contains both tabs and spaces (if necessary), while the part defined by alignment consists only of spaces.
  * If this checkbox is cleared, only tabs are used. This means that after reformatting a group of spaces that fits the specified tab size is automatically replaced with a tab, which may result in breaking fine alignment.

The Smart Tabs checkbox is available if the Use tab character checkbox is selected.  
Tab size| In this field, specify the number of spaces that fits in a tab.  
Indent| In this field, specify the number of spaces to be inserted for each indent level.  
Continuation indent| In this field, specify the number of spaces to be inserted between the elements of an array, in expressions, method declarations, and method calls.  
Keep indents on empty lines| If this checkbox is selected, IntelliJ IDEA retains indents on empty lines as if they contained some code. If the checkbox is cleared, IntelliJ IDEA deletes the tab characters and spaces on empty lines.  
Indent children of top-level tag| By default, only the code inside `template` tags has initial indentation. If necessary, add other tags using commas as separators. For example, if you specify `script` in the field, the code inside all `script` tags gets initial indentation as shown in the Preview pane. 
