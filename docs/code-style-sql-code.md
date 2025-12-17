[//]: # (Source: https://www.jetbrains.com/help/idea/code-style-sql-code.html)
[//]: # (Downloaded: 2025-12-17 19:20:37)

# Code

Configure code style for declared variables, routine arguments, routine statements, loops, and other structures.

Use this page to configure formatting options for SQL files. When you change these settings, the Preview pane shows how this will affect your code.

Item| Description  
---|---  
Wrap every statement| Place every statement on a new line.  
Keep blank lines in code| Set the maximum number of blank lines between instructions. If you put more lines than declared in this option, additional lines are deleted automatically.  
Put new line around semicolon| Move a semicolon to a new line. Works only for semicolons between statements.  
  
Item| Description  
---|---  
Wrap section| Move declaration section to a new line.  
Wrap variables| Move elements to a new line.

  * Chop: move each value to a new line.
  * Chop if long: move each value to a new line if the text exceeds the configured line length. To configure the line length, open settings `Ctrl+Alt+S`, navigate to Editor | Code Style, and type the necessary length in the Hard wrap at N columns field. 
  * Wrap if long: break a section of text into lines so that each line fits the configured line length. To configure the line length, open settings `Ctrl+Alt+S`, navigate to Editor | Code Style, and type the necessary length in the Hard wrap at N columns field. 

  
Align types| Align variable types.  
Align assignments| Align variable assignments (for example, `:=`).  
Align expressions| Align assigned values.  
  
Item| Description  
---|---  
Place the opening parenthesis| Align or indent the opening parenthesis under the first keyword on the line. Select On the same line to keep the opening parenthesis on the line with the keyword.  
Place elements| Change the position of elements in parentheses.

  * Same line aligned: align all members of the clause, keep the first member on the same line with a parenthesis.
  * Wrapped unindented: move all members of the clause to a new line without adding an indent.
  * Wrapped aligned: align and move all members of the clause to a new line.
  * Wrapped indented: add an indent and move all members of the clause to a new line.

  
Place the closing parenthesis| Change the position of the closing parenthesis. You can position the closing parenthesis relative to the opening parenthesis (Under opening), or the first element after the opening parenthesis (Under elements).  
Wrap elements| 

  * Chop: move each value to a new line.
  * Chop if long: move each value to a new line if the text exceeds the configured line length. To configure the line length, open settings `Ctrl+Alt+S`, navigate to Editor | Code Style, and type the necessary length in the Hard wrap at N columns field. 
  * Wrap if long: break a section of text into lines so that each line fits the configured line length. To configure the line length, open settings `Ctrl+Alt+S`, navigate to Editor | Code Style, and type the necessary length in the Hard wrap at N columns field. 

  
Place comma| Move a comma (`,`) to the beginning (To begin) or to the end (To end) of a code line.The Auto option analyzes the surrounding context and calculates the most suitable place for a comma. For example, you have three occurrences of a comma: two commas go at the beginning, one comma is at the end. The Auto option will move the third occurrence of the comma to the beginning. This option works only if you have more than three cases in a single context. Otherwise, commas are left as is.The In the middle option joins two lines of code on one line.If you want to disable a new line after the comma when the To begin option is enabled, clear the Line breaks checkbox on the Wrapping tab.  
Put spaces within parentheses| Add a space after the opening parenthesis and before the closing parenthesis.  
Align types| Align variable types.  
  
Item| Description  
---|---  
Wrap AS| Move AS to a new line.  
Wrap opening $$| Move the opening dollar quoting to a new line.  
Wrap the content after opening $$| Move the content after the opening dollar quoting.  
Wrap before closing $$| Move the closing dollar quoting to a new line.  
Wrap options after closing $$| Move options after the closing dollar quoting to a new line.  
  
Item| Description  
---|---  
Wrap THEN| Move THEN to a new line.  
Wrap ELSE| Move ELSE to a new line.  
Wrap inner code| Move inner code to a new line.  
Indent THEN and ELSE| Add an indent before THEN and ELSE.  
Indent END IF| Add an indent before END IF.  
Collapse when short| Join multiline short constructions. The length of a construction that will be collapsed is determined automatically by IntelliJ IDEA.  
  
Item| Description  
---|---  
Wrap LOOP| Move LOOP to a new line.  
Indent LOOP| Add an indent before LOOP.  
Indent END LOOP| Add an indent before END LOOP.  
Collapse when short| Join multiline short constructions. The length of a construction that will be collapsed is determined automatically by IntelliJ IDEA.  
  
27 January 2025

[DDL](code-style-sql-ddl.html)[Expressions](code-style-sql-expressions.html)
