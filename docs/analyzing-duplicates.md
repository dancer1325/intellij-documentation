[//]: # (Source: https://www.jetbrains.com/help/idea/analyzing-duplicates.html)
[//]: # (Downloaded: 2025-12-17 19:18:11)

## Locate duplicates manually (deprecated)

  1. In the main menu, go to Code | Analyze Code | Locate Duplicates.

  2. In the [Specify Code Duplication Analysis Scope](#specify-code-duplication-analysis-scope) dialog, choose the analysis [scope](configuring-scopes-and-file-colors.html): the whole project, the current file, uncommitted files (for projects under version control), or a custom scope. You can also choose to include test sources in the analysis.

  3. In the [Code Duplication Analysis Settings](#code-duplication-analysis-settings) dialog, select the languages that you want to analyze.

For each language, check the options to define the analysis preferences. For example, you can opt to request identical match for code fragments to be considered duplicates, or specify a certain limit below which the code constructs are not considered duplicates (for example, to avoid reporting each `if` construct in the source code).

![Code Duplication Analysis Settings](https://resources.jetbrains.com/help/img/idea/2025.3/code-duplication-analysis-settings.png)
  4. In the [Duplicates tool window](duplicates-tool-window.html), explore the analysis results.

![Duplicates tool window](https://resources.jetbrains.com/help/img/idea/2025.3/duplicates.png)



### Specify Code Duplication Analysis Scope

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
  
### Code Duplication Analysis Settings

Use this dialog to define the sensitivity of search and set the limitation that will help you avoid reporting every similar code construct. Your preferences are specified in a language-specific context.

Item| Description  
---|---  
Java| To anonymize an element means to define whether identical entities that only differ by names or values should be treated as duplicates. Select elements to anonymize:

  * Anonymize Literals
  * Anonymize Local Variables
  * Anonymize Fields
  * Anonymize Methods
  * Anonymize Types

Configure duplicate parameters:

  * Do not show duplicates simpler than: Set the size of duplicated language constructs that are shown in the result window. By default, the constructs less than 10 units are not included (and this limitation cannot be changed).
  * Visible from outside of the scope only: If this checkbox is selected, verify that the discarded subelement is valid outside the current construct. If the subelement is senseless, it cannot be discarded and should not be considered duplicated.
  * Anonymize uncommon subexpressions simpler than: Set the value of the subelements within language constructs that can be considered similar, to show the construct as duplicate in the result window. The larger is the number, the larger constructs are taken as similar by IntelliJ IDEA.The values are set as arbitrary weights based on the element size calculated with additive algorithm. The larger the element, the higher is the calculated value.

  
ActionScriptECMAScript 6Flow JSGroovyJavaScriptTypeScriptTypeScript JSX| To anonymize an element means to define whether identical entities that only differ by names or values should be treated as duplicates. Select elements to anonymize:

  * Anonymize Variables
  * Anonymize Literals
  * Anonymize Functions

Configure duplicate parameters:

  * Do not show duplicates simpler than: Set the size of duplicated language constructs that are shown in the result window. By default, the constructs less than 10 units are not included (and this limitation cannot be changed).
  * Anonymize uncommon subexpressions simpler than: Set the value of the subelements within language constructs that can be considered similar, to show the construct as duplicate in the result window. The larger is the number, the larger constructs are taken as similar by IntelliJ IDEA.The values are set as arbitrary weights based on the element size calculated with additive algorithm. The larger the element, the higher is the calculated value.

  
CSS| 

  * Do not show duplicates containing less than <number> CSS properties: Set the size of duplicated language constructs that are shown in the results window.

  
XHTMLXMLHTML| 

  * Do not show duplicates containing less than <number> tags: Set the size of duplicated language constructs that are shown in the results window.
  * Anonymize values of tags and attributes


