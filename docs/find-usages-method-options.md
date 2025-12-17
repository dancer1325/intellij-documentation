[//]: # (Source: https://www.jetbrains.com/help/idea/find-usages-method-options.html)
[//]: # (Downloaded: 2025-12-17 19:27:03)

# Find Usages. Method Options

This section describes the controls for specifying Method Usage Search options in the Find Usages dialog.

You can also open this dialog when you click ![Settings](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) in the Show Usages popup which lists all the occurrences of the symbol at caret.

With the Usages option, the base method will be included in the search results automatically. 

Item| Description  
---|---  
Find| In this area, specify the objects to search. 

  * Usages: select this option to search for all references of the method by its name.
  * Search for base method usages: if you select this option for the method that has ancestors, meaning this method overrides some base method, the usages of the method itself and the usages of base methods will be found. If you don't select this option, the usages of only the method in question will be found. The usages of base methods will not be included in the results of the search.
  * Overriding methods: select this option to search for all methods that override the selected method.
  * Implementing methods: select this option to search for all methods that implement the selected method.

  
Text occurrences| Select this checkbox to search in for the occurrences in text files.  
Skip results tab with one usage| Select this checkbox to be navigated directly to the found usage without the Find tool window displayed when only one usage is found.  
Scope| In this area, specify the scope of search. Select a pre-defined scope from the list or click the Browse button ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) to open the [Scopes](settings-scopes.html) dialog, where you can define a custom scope.  
Open results in new tab| Select this checkbox to have the results of each search shown in a separate tab of the Find Results window. If the checkbox is cleared, the search results will overwrite the contents of the current tab.  
  
08 October 2024

[Find Usages. Class Options](find-usages-class-options.html)[Find Usages. Package Options](find-usages-package-options.html)
