[//]: # (Source: https://www.jetbrains.com/help/idea/find-usages-class-options.html)
[//]: # (Downloaded: 2025-12-17 19:27:00)

# Find Usages. Class Options

This section describes the controls for specifying Class Usage Search and Interface Usage Search options in the Find Usages dialog.

The dialog opens when you click ![the Show settings icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.gear.svg) in the Show Usages popup which lists all the occurrences of the symbol at the caret.

Item| Description  
---|---  
Find| In this area, specify the objects to search. 

  * Usages \- if this checkbox is selected, the search is performed for all references of the class by its name.
  * Usages of methods \- if this checkbox is selected, the search is performed for all calls of the selected class methods.
  * Usages of fields \- if this checkbox is selected, the search is performed for usages of selected class fields.
  * Derived classes \- if this checkbox is selected, the search is performed for all classes that extend the selected class. The checkbox is available for class usage search only.
  * Implementing classes \- if this checkbox is selected, the search is performed for all classes that implement the selected interface. The checkbox is available for interface usage search only.
  * Derived interfaces \- if this checkbox is selected, the search is performed for all interfaces that extend the selected interface. The checkbox is available for interface usage search only.

  
General| In this area, configure the search procedure using the following controls: 

  * Search for text occurrences \- if this checkbox is selected, the search is performed in files registered in IntelliJ IDEA.
  * Skip results tab with one usage \- select this checkbox to be navigated directly to the found usage without the Find tool window displayed when only one usage is found.

  
Scope| In this area, specify the [scope](configuring-scopes-and-file-colors.html) of search. Select a pre-defined scope from the list or click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) to open the [Scopes](settings-scopes.html) dialog, where you can define a custom scope.  
Open in new tab| Select this checkbox to have the results of each search shown in a separate tab of the Find tool window. If the checkbox is cleared, the search results will overwrite the contents of the current tab.  
  
08 October 2024

[Find Usages](find-usages-dialog.html)[Find Usages. Method Options](find-usages-method-options.html)
