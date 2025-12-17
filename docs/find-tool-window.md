[//]: # (Source: https://www.jetbrains.com/help/idea/find-tool-window.html)
[//]: # (Downloaded: 2025-12-17 19:26:59)

## Toolbar buttons

Item| Tooltip and Shortcut| Description  
---|---|---  
![the Settings button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg)| Options`Ctrl+Alt+Shift+F7`|  Click this button to open one of the Find Usages dialogs, which corresponds to the symbol. You can edit the search settings and click Rerun button to execute the modified search query.   
![the Rerun button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.rerun.svg)| Rerun`Ctrl+F5`| Repeat the last search. This button is not available for [viewing code coverage results](code-coverage.html#read_the_coverage_data).   
![the Close button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.closeSmall.svg)| Close`Ctrl+Shift+F4`| Close the current tab or the tool window. This button is not available in Replace in Path and Refactoring Preview dialogs.   
![](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.pin_tab.svg)| Pin Tab| Click this button to pin or unpin the current tab. You may need to pin a tab to prevent it from closing automatically when the maximum number of tabs is reached in this window.  
![Expand all](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.expandAll.svg)/![Collapse all](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.collapseAll.svg)| Expand all `Ctrl+NumPad +`Collapse all `Ctrl+NumPad -`| Use these buttons to have all nodes expanded or collapsed.  
![Previous occurrence](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.up.svg)/![Next occurrence](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.down.svg)| Previous/next occurrence`Ctrl+Alt+Up``Ctrl+Alt+Down`| Navigate to the previous/next element in the tab of results.  
![Group by](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.groupBy_dark.svg)| Group by| Click this icon to open the menu for the following grouping options:

  * File Structure `Ctrl+S`: select this option to display the found usages under the corresponding method nodes. 
  * Module `Ctrl+Alt+M`: if you select this option, the found usages will show under the corresponding module or the library node.This type of grouping is helpful, when a package is split between several modules.
  * Flatten Modules`Alt+O`: select this option to display all the modules as a single-level tree view.
  * Package `Ctrl+P`: select this option to display all the found usages under their respective packages. 
  * Directory Structure `Ctrl+Alt+D`: select this option to show all the usages of a symbol under the directories where they are found.
  * Test/Production: select this option to group the usages according the Production and Test scopes.
  * Usage type `Ctrl+T`: if this option is selected, the search results are grouped by the following categories: 
    * instanceof
    * import
    * cast target type
    * extends/implements clause
    * class static member access
    * method throws list
    * .class
    * field declaration
    * local variable declaration
    * method parameter declaration
    * catch clause parameter declaration
    * method return type
    * delegates to another object instance
    * delegates to another object instance with different parameters
    * delegates to super
    * delegates to super with different parameters
    * recursive method calls
    * string constants
    * comments
    * unclassified usage not related to any of the categories
  * Merge Usages from the Same Line: select this option to merge the duplicate usages found on the same line.

  
![Show read access](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.showReadAccess.svg)| Show read access`Ctrl+R`| This button is available for Find Usages only.If this button is pressed, the search results include references to the read access methods.  
![Show write access](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.showWriteAccess.svg)| Show write access`Ctrl+W`| This button is available for Find Usages only.If this button is pressed, the search results include references to the write access methods.  
![Show import statements](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.showImportStatements.svg)| Show import statements`Ctrl+I`| This button is available for Find Usages only.If this button is pressed, the search results include the usages in the import statements.  
![the Preview Usages button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.previewDetails.svg)| Preview Usages|  Click this icon to open the Preview pane next to the search results.   
The following buttons are available for Replace in Path only.  
Do Replace All| `Alt+D`| Click this button to replace all occurrences in the current tab of results.  
Replace Selected| `Alt+L`| Click this button to replace the selected occurrence in the current tab of results.  
The following buttons are available for Refactoring Preview only.  
Do Refactor| `Alt+D`| Click this button to perform refactoring on all occurrences in the current search results.  
Cancel| `Alt+C`| Click this button to discard search results and close the results tab.  
The following buttons are available for Structural Replace only.  
Replace All| | Click this button to replace all found occurrences.  
Replace Selected| | Click this button to replace the highlighted occurrence.  
Preview Replacement| | Click this button to show how the changes will apply to the selected node in the Find tool window. In this case, the corresponding occurrence is highlighted in the source code.
