[//]: # (Source: https://www.jetbrains.com/help/idea/extract-variable-refactoring-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:26:38)

# Extract Variable dialog

Generally, this dialog is used to extract new variables. Depending on the language, there may be additional options.

  * In Java, you can declare the new variable `final`.

To make this dialog accessible for Java, you have to disable [in-place refactoring in the editor settings](code-editing.html#in_place_refactorings).

  * In JavaScript, you can select to extract a (global) variable or a constant. For JavaScript 1.7, JavaScript 1.8.5, ES5, and ES6, there is also an option of extracting a local variable.




Item| Description| Language  
---|---|---  
Type| Select the type of the new variable.| ActionScript  
Name| Specify the name for the new variable.| All  
Replace all occurrences| Select this option to replace all the occurrences of the selected expression (if more than one occurrence of the selected expression is found).| All  
Declare final| Select this option to declare the new variable `final`.| Java  
| Choose how to extract the variable:

  * var – extract a global variable.
  * const – extract a constant.
  * let – extract a local variable. The let option is available only for JavaScript 1.7, JavaScript 1.8.5, ES5, and ES6.

| JavaScript  
Make constant| Select this option to extract a constant rather than a variable.| ActionScript  
  
02 September 2025

[Extract Superclass Dialog](extract-superclass-dialog.html)[Move dialogs](move-dialogs.html)
