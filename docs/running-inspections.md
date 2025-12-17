[//]: # (Source: https://www.jetbrains.com/help/idea/running-inspections.html)
[//]: # (Downloaded: 2025-12-17 19:59:25)

## Run inspections manually

Some inspections require global code analysis, and that is why they are disabled in the editor. These inspections are listed in Settings | Editor | Inspections. Click ![Filter Inspections](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.filter.svg) and select Show only batch-mode inspections.

If you want to get a full report of all problems in your code, run inspections manually. In this case, the IDE runs all inspections enabled in your [inspection profile](customizing-profiles.html) and shows you the result in a dedicated tool window. The time required to finish the analysis depends on the number of enabled inspections and the size of the scope that you're analyzing.

### Run all inspections

  1. In the main menu, go to Code | Inspect Code.

  2. Select the [scope](#Specify-inspection-scope) of files that you want to analyze.

Click the ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) icon to configure a new scope.

  3. Select the [inspection profile](customizing-profiles.html) that you want to apply.

To create a new profile or modify one of the existing profiles, click Configure.

  4. Click Analyze to start the analysis.


![The Specify Inspection Scope dialog](https://resources.jetbrains.com/help/img/idea/2025.3/inspection_scope.png)

### Specify Inspection Scope dialog

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
Inspection profile| Select a [profile](customizing-profiles.html) that you want to use to inspect your code.If the required profile is not in the list, click Configure and create a new profile.  
  
### Run a single inspection

Running a single inspection is useful in case you want to track a specific problem. If you find a warning in a file, you can inspect your entire project, or the necessary scope of files, to ensure that there are no more such warnings in your code base.

  1. Press `Ctrl+Alt+Shift+I` or go to Code | Analyze Code | Run Inspection by Name in the main menu.

  2. Type the inspection name in the popup. Use CamelHumps to match camel case words and white spaces with initial letters of the words. The suggestion list will show you inspections that match your search request.

If you are not sure that you are selecting the correct inspection, you can view its description. To do so, select an inspection in the popup and press `Ctrl+Q`.

  3. Double-click the necessary inspection.

  4. In the dialog that opens, select the scope of files that you want to analyze.

The File mask(s) option helps you narrow down the number of files that will be inspected.

Select the checkbox and specify a pattern of characters and wildcards that matches the names of files you want to analyze. Use a comma to separate multiple file masks.

  5. Some inspections might have additional options that you will be prompted to configure.

These settings will only be applied to this run and will not affect this inspection's configuration in your current profile.

The IDE will show you the inspection results in the dedicated tool window tool window. There you can examine and fix detected problems.



