[//]: # (Source: https://www.jetbrains.com/help/idea/using-live-templates.html)
[//]: # (Downloaded: 2025-12-17 20:05:30)

## Types of live templates

The following types of live templates are distinguished:

  * Simple templates contain only fixed plain text. When you expand a simple template, the text is automatically inserted into your source code, replacing the abbreviation. 

Abbreviation| Expands to  
---|---  
`psfs`|  public static final String   
`main` or `psvm`|  public static void main(String[] args){ }   
`sout`|  System.out.println();   
  
  * Parameterized templates contain [variables](template-variables.html) that enable user input. When you expand a parameterized template, variables are either replaced by input fields for the user to specify manually, or calculated by IntelliJ IDEA automatically. 

Abbreviation| Expands to  
---|---  
`for`|  for (int i = 0; i < ; i++) { }   
`ifn`|  if (var == null) { }   
  
  * Surround templates wrap a block of the selected code with the text specified by the user. For example, `T` expands into a pair of tags, for which you can specify a name. You can also select a block of code, then press `Ctrl+Alt+J` to open the Select Template popup and select the `T` template to wrap the selection with a pair of tags. 




[Postfix code completion](postfix-code-completion.html) is similar to live templates. It transforms the current expression without selecting it. For example, you can type `.if` after an expression to invoke the corresponding postfix completion and wrap the expression with an `if` statement. 
