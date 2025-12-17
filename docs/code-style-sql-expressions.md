[//]: # (Source: https://www.jetbrains.com/help/idea/code-style-sql-expressions.html)
[//]: # (Downloaded: 2025-12-17 19:20:40)

# Expressions

Configure code style for corteges, binary expressions, the `CASE` clause, and procedure calls.

Use this page to configure formatting options for SQL files. When you change these settings, the Preview pane shows how this will affect your code.

Item| Description  
---|---  
Add space before '('| Add space before the opening parenthesis (`(`).  
Space within parentheses| Add a space after the opening parenthesis and before the closing parenthesis.  
Place comma to begin| Move a comma to a new line.  
Space before comma| Add a space before a comma.  
Space after comma| Add a space after a comma.  
  
Item| Description  
---|---  
Use spaces around operators| Add a space before and after an operator.  
Align operands in binary expressions| Align operands in binary expressions.  
Space between parenthesized sub-expressions| Add a space after the opening parenthesis and before the closing parenthesis in subexpressions.  
  
Item| Description  
---|---  
Space within parentheses| Add a space after the opening parenthesis and before the closing parenthesis  
Space before comma| Add a space before a comma.  
Space after comma| Add a space after a comma.  
  
Item| Description  
---|---  
Wrap WHEN| Move WHEN to a new line.  
Indent WHEN if wrapped| Add an indent before WHEN if the Wrap WHEN option is selected.  
Wrap THEN| Move THEN to a new line.  
Align THEN| Align all THEN keywords in CASE clauses.  
Align ELSE under THEN when THEN aligned| Align ELSE under THEN when THEN is aligned.  
Align END| Align END in CASE clauses.

  * Align with CASE: align END with CASE keyword.
  * Align with WHEN: align END with CASE keyword.
  * To end: move END at the end of code section to the same line.

  
Keep new line after THEN, ELSE| Add a new line after THEN and ELSE.  
Collapse short clause| Join multiline short clauses. The length of a clause that will be collapsed is determined automatically by IntelliJ IDEA.  
  
27 January 2025

[Code](code-style-sql-code.html)[Tabs and Indents](code-style-sql-tabs-and-indents.html)
