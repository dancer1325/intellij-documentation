[//]: # (Source: https://www.jetbrains.com/help/idea/settings-smart-keys.html)
[//]: # (Downloaded: 2025-12-17 20:01:47)

# Smart Keys

Use this page to enable or disable specific [smart keys](using-code-editor.html#smart-keys) and to define which actions you want to be invoked automatically.

Item| Description  
---|---  
Home moves caret to first non-whitespace character| When this checkbox is selected, on pressing `Home`, the caret is positioned at the first non-whitespace character of the current line. Pressing `Home` subsequently moves the caret from the _Smart Home position_ to the first column and back.  
End on blank line moves caret to indent position| When this checkbox is selected, on pressing `End` in an empty line, the caret is positioned with the indent, which IntelliJ IDEA assumes to be reasonable in the current code point (indentation is based on the current [Code Style Settings](settings-code-style.html)).  
Insert pair brackets (), [], {}, <>| Select this checkbox to have IntelliJ IDEA automatically add a closing bracket for each typed opening bracket, respectively.  
Insert pair quote| Select this checkbox to have IntelliJ IDEA automatically add a closing single or double quote for each typed opening single or double quote, respectively.   
Reformat block on typing '}'| If this checkbox is selected, then, on typing the closing curly brace, the enclosed code block is reformatted automatically if the formatting of this code block does not match the selected code style.  
Use "CamelHumps" words| Select this checkbox to have IntelliJ IDEA discern separate words within CamelHump names. Words within a name should start with a capital letter or an underscore. This option impacts some editor actions, for example:

  * Caret Move `Ctrl+Right`/`Ctrl+Left`
  * Caret Move with Selection (`Ctrl+Shift+Right`/`Ctrl+Shift+Left`)
  * Select Word at Caret `Ctrl+W`
  * Delete to Word Start/End (`Ctrl+Backspace` and `Ctrl+Delete` respectively)
  * Double-clicking (if Honor "CamelHumps" word settings when selecting using double click is enabled).

IntelliJ IDEA also provides similar actions that work in a mode opposite to the one selected in the Use 'CamelHumps' words setting:

  * Move Caret to Previous Word in Different "CamelHumps" mode
  * Move Caret to Previous Word with Selection in Different "CamelHumps" mode
  * Move Caret to Next Word in Different "CamelHumps" mode
  * Move Caret to Next Word with Selection in Different "CamelHumps" mode
  * Delete to Word End in Different "CamelHumps" mode
  * Delete to Word Start in Different "CamelHumps" mode

For example, if Use 'CamelHumps' words is _enabled_ , the action Move Caret to Next Word in Different "CamelHumps" mode moves the caret to the end of word regardless of uppercase characters in this word; if Use 'CamelHumps' words is _disabled_ , then the caret moves to the next CamelHump within this word.These actions have no default keyboard shortcuts and are not included in the menus, but you can invoke them from [Go to Action](searching-everywhere.html#find_action) `Ctrl+Shift+A`:![Alternative actions for CamelHump navigation](https://resources.jetbrains.com/help/img/idea/2025.3/camelHumpsActions.png)You can bind them with the shortcuts of your choice as described in the section [Configure keyboard shortcuts](configuring-keyboard-and-mouse-shortcuts.html).  
Honor "CamelHumps" words settings when selecting on double click| Select this checkbox to have IntelliJ IDEA invoke the CamelHumps selection when words are selected by double-clicking.This feature works only if the [Use 'CamelHumps' words](#camelHumps) option is enabled.  
Surround selection on typing quote or brace| If this checkbox is selected, the selected text on typing a quote, double-quote or brace, will be surrounded with these characters. If this checkbox is not selected, then the typed quotes, double-quotes or braces will replace the selection.  
Add multiple carets on double `Ctrl` with arrow keys| If this checkbox is selected, then:

  * pressing `Ctrl` plus up/down arrow keys leads to creating multiple carets.
  * pressing `Ctrl` plus left/right arrow keys or Home/End leads to creating a selection.

For more information, refer to the [Multicursor](working-with-source-code.html#editor_lines_code_blocks) section.  
Jump outside closing bracket/quote with Tab when typing| If this checkbox is selected, pressing `Tab` when typing inside brackets/quotes will move the caret outside the closing bracket/quote. If this checkbox is not selected, pressing `Tab` will insert the `Tab` character.Note that this only works on initial typing: during subsequent editing, pressing `Tab` inside brackets/quotes will insert the `Tab` character.  
Enter| Use this area to define the actions to be invoked by pressing `Enter`.

  * Smart indent: select this checkbox to have IntelliJ IDEA add a new line and place the caret at it, with the indent that IntelliJ IDEA assumes to be reasonable in the current point of code (indentation is based on the current [Code Style](settings-code-style.html) settings).If the checkbox is cleared, upon pressing `Enter` in a blank line, IntelliJ IDEA adds a new line and positions the caret at the current non-space character column.
  * Insert pair '}': select this checkbox to have IntelliJ IDEA automatically position a closing brace `}` at the proper column when `Enter` is pressed in an empty line. In this case IntelliJ IDEA seeks backward for the nearest unclosed opening brace `{` and places the closing one at the corresponding indentation level.
  * Close block comment: unselect this checkbox to disable the automatic closure of the block comment when hitting `Enter`.
  * Insert documentation comment stub: this checkbox defines the behavior on pressing `Enter` after the opening documentation comment. This functionality works only for JavaScript , Java, Groovy, and Swift. 
    * If this checkbox is selected, IntelliJ IDEA generates a documentation comment stub.For the method comments, this stub contains the required tags (`@param` tags for each method parameter, `@return`, or `@throws`). For more information, refer to [Javadocs](javadocs.html) and [JSDoc comments](creating-jsdoc-comments.html).
    * If this checkbox is not selected, only the closing part of the comment is generated.
Note that this checkbox refers to JavaScript, Java, and other languages that have special beginning of documentation comments.

  
Unindent on Backspace| Use this list to define the actions to be invoked by pressing `Backspace` key. The available options are:

  * Disabled: pressing `Backspace` returns the caret by one position at a time.
  * To nearest indent position
  * To proper indent position

  
Reformat on paste| Use this list to specify how to place pasted code blocks. The available options are:

  * None: the pasted code is inserted at the caret location as plain text without any reformatting or indenting.
  * Indent block: the pasted code block is positioned at the proper indentation level, according to the current [Code Style Settings](settings-code-style.html), but its inner structure is not changed.
  * Indent each line: each line of the pasted code block is positioned at the proper indentation level, according to the current Code Style Settings.
  * Reformat block: the pasted code block is reformatted according to the current Code Style Settings.

This feature is applicable to lines that contain the trailing line feed characters.  
Reformat again to remove custom line breaks| When this option is enabled, invoking the [Reformat Code](reformat-and-rearrange-code.html#reformat_code) `Ctrl+Alt+L` or [Reformat File](reformat-and-rearrange-code.html#reformat_file) `Ctrl+Alt+Shift+L` actions the second time after the code has been reformatted will remove custom line breaks.When the option is disabled, invoking the actions the second time opens a dialog in which you need to confirm removing line breaks first. Click Don't ask again in the dialog to never remove custom line breaks when you reformat code for the second time.  
JavaDoc| Use this area to configure smart keys options for JavaDoc.

  * Automatically insert closing tag in JavaDoc: select this option if you want IntelliJ IDEA to add a closing tag for your code in the JavaDoc comments. In this case IntelliJ IDEA places the caret inside the tag. For example, if you type `<b>`, the closing tag `</b>` will be generated automatically.

  
Insert pair '%>' on Enter in JSP| Select this checkbox to have IntelliJ IDEA automatically position the opening angle bracket `<` at the proper column when entered in an empty line in JSP code. In this case IntelliJ IDEA seeks backward for the nearest unclosed angle bracket and places a closing one `>` at the corresponding indentation level.  
Kotlin| Use this area to configure the smart keys options for Kotlin.

  * Convert pasted Java code to Kotlin: select this option to convert any Java code to Kotlin on paste. IntelliJ IDEA displays the Convert Code from Java dialog. If you don't want IntelliJ IDEA to show the dialog, select the Don't show Java to Kotlin conversion dialog on paste option.

  
  
29 May 2025

[Postfix Completion](settings-postfix-completion.html)[Smart Keys settings: HTML/CSS](settings-smart-keys-html-css.html)
