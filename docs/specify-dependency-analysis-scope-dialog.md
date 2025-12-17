[//]: # (Source: https://www.jetbrains.com/help/idea/specify-dependency-analysis-scope-dialog.html)
[//]: # (Downloaded: 2025-12-17 20:02:52)

# Specify Dependency Analysis Scope dialog

Use this dialog to define the scope for the search of dependencies or nullable elements. The contents of the dialogs slightly differ depending on the type of analysis.

Item| Description  
---|---  
Whole project| Inspect the whole project.  
Module <name>| Inspect the module that is currently selected in the Project tool window `Alt+1`.  
File <name>| Inspect the file that is currently selected in the Project tool window or opened in the editor.  
Selected files| Inspect the files that are currently selected in the Project tool window.  
Uncommitted files| This scope is only available for the projects under version control.Inspect only the files that have not been committed to the version control system.  
Directory| Inspect the directory that is currently selected in the Project tool window.  
Custom scope| Inspect a custom scope of files. Select a pre-defined scope from the list, or click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and define the scope in the [Scopes dialog](settings-scopes.html) that opens.Use a special [language](scope-language-syntax-reference.html) to define a scope.  
Include test sources| Inspect the test sources included in the analysis scope.  
Inspect injected code| Inspect [pieces of code in other languages](using-language-injections.html) embedded in your code.  
Show transitive dependencies. Do not travel deeper than| Select this checkbox to have IntelliJ IDEA analyze transitive dependencies. From the Do not travel deeper than list, choose the desired level.The field is available for the dependencies analysis only.  
Annotate local variables| If this checkbox is selected, then the local variables of a class will be included in the nullity analysis, and annotated.The field is available for [inferring nullity](annotating-source-code.html#infer-nullity) only.  
  
11 February 2024

[Dependencies analysis](dependencies-analysis.html)[Dependency Structure Matrix](dsm-analysis.html)
