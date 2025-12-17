[//]: # (Source: https://www.jetbrains.com/help/idea/compiler-excludes.html)
[//]: # (Downloaded: 2025-12-17 19:21:20)

# Excludes

Use this page to specify files and directories within your project that should not be passed to the compiler.

Item| Keyboard Shortcut| Description  
---|---|---  
Path| | In this field, the path to a file or directory to be excluded from compilation is shown.  
Recursively| | For a directory: select this option to exclude from compilation all the corresponding subdirectories.  
![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)| `Alt+Insert`| Use this icon or shortcut to add a file or directory to the list. Select the file or directory in the dialog that opens.  
![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)| `Alt+Delete`| Use this icon or shortcut to remove the selected item or items from the list.  
  
  * The sources listed on this page, if they are used in the project parts to be compiled (for example, if they are imported, extended or implemented), will nevertheless be compiled.

  * Explicit compiler invocation on excluded directories will force their compilation.




11 October 2024

[Nullable/NotNull configuration dialog](nullable-notnull-configuration.html)[Java Compiler](java-compiler.html)
