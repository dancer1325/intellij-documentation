[//]: # (Source: https://www.jetbrains.com/help/idea/code-editing.html)
[//]: # (Downloaded: 2025-12-17 19:20:13)

# Code Editing

Use the Code Editing page of the Settings dialog to configure the general code editing options.

Item| Description  
---|---  
Highlight on Caret Movement  
Matched brace| Select this checkbox to have IntelliJ IDEA highlight pairs of opening/closing braces when you place the caret right before the opening or right after the closing one. It also works for HTML and XML tags.  
Current scope| Select this checkbox to have IntelliJ IDEA highlight the available scope for the code typed in the current caret location.  
Usages of element at caret| Select this checkbox to have IntelliJ IDEA highlight all usages of the element at which the caret is currently positioned.  
Refactorings  
Specify refactoring options| 

  * In the editor: select this option to enable the in-place refactoring mode for Java. In the in-place mode, you specify all or most of the information necessary for the refactoring just by typing it, right in the editor. All the affected code fragments are highlighted and change as you type. If appropriate, additional refactoring options are selected in corresponding option boxes.The in-place refactoring mode is available for the following refactorings:
    * [Extract Constant](extract-constant.html)
    * [Extract Field](extract-field.html)
    * [Extract Parameter](extract-parameter.html)
    * [Extract Method](extract-method.html)
    * [Extract Variable](extract-variable.html)
    * [Rename](rename-refactorings.html)
  * In modal dialogs: select this option if you want to use the refactoring dialogs when you refactor code.

  
Preselect current symbol name for Rename refactoring| If this checkbox is selected, the old name of a symbol is selected in the editor or in the Rename dialog when the [Rename refactoring](rename-refactorings.html) is invoked for that symbol.If the checkbox is cleared, the symbol to be renamed is not selected.   
Show inline dialog for local variables| Select this checkbox if you want to display a confirmation dialog for the Inline local variable refactoring.  
Error Highlighting  
Error stripe mark min height (pixels)| In this field, specify the minimum size of the error and warning stripes.  
Autoreparse delay (ms)| In this field, specify the time period after which IntelliJ IDEA starts reparsing the entered text.  
The 'Next Error' action goes through| 

  * The problems with the highest priority: select this option to have IntelliJ IDEA pass through the highest priority problems only (for example, errors), when executing Navigate | Next/Previous Highlighted Error command `F2`/`Shift+F2`.
  * All problems: select this option to have IntelliJ IDEA pass through all the existing problems (for example, errors and warnings) sequentially.

  
Suppress with @SuppressWarnings (for 5.0 only)| Select this checkbox to have `@SuppressWarnings` implemented as an annotation.Clear this checkbox to have `@SuppressWarnings` implemented as a Javadoc comment.  
Quick Documentation  
Show quick documentation on hover| Select this checkbox to [show quick documentation](viewing-reference-information.html#inline-quick-documentation) for the symbol when you move the mouse pointer over it. The quick documentation popup appears after the delay time specified in the Tooltip delay field.  
Editor Tooltips  
Tooltip delay| Use this option to specify the delay, with which all editor tooltips appear on mouse hover. Editor tooltips include:

  * Quick Documentation, which appears if the Show quick documentation on hover option is selected above on this settings page. You can press `Ctrl+Q` to invoke this tooltip with the keyboard.
  * Error description, which appears on highlighted code issues if the design-time code inspection is enabled for the current file. You can press `Ctrl+F1` to invoke this tooltip with the keyboard.

You can copy the full contents of the tooltip by `Alt`-clicking it (`Ctrl+Alt`-clicking it if you are on Linux).  
  
02 May 2025

[Smart Keys settings: Twig](settings-smart-keys-twig.html)[Font settings](settings-editor-font.html)
