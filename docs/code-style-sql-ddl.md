[//]: # (Source: https://www.jetbrains.com/help/idea/code-style-sql-ddl.html)
[//]: # (Downloaded: 2025-12-17 19:20:39)

# DDL

Configure code style for `CREATE`, `ALTER`, views, constraints, and other DDL structures.

Use this page to configure formatting options for SQL files. When you change these settings, the Preview pane shows how this will affect your code.

Item| Description  
---|---  
Place the opening parenthesis| Align or indent the opening parenthesis under the first keyword on the line. Select On the same line to keep the opening parenthesis on the line with the keyword.  
Place elements| Change the position of elements in parentheses.

  * Same line aligned: align all members of the clause, keep the first member on the same line with a parenthesis.
  * Wrapped unindented: move all members of the clause to a new line without adding an indent.
  * Wrapped aligned: align and move all members of the clause to a new line.
  * Wrapped indented: add an indent and move all members of the clause to a new line.

  
Place the closing parenthesis| Change the position of the closing parenthesis.

  * At the end: place the closing parenthesis at the same line with the last element of a clause.
  * To begin: move the closing parenthesis to a new line with the last element of a clause.
  * Under opening: place the closing parenthesis under the opening parenthesis.
  * Under elements: place the closing parenthesis under aligned elements of a clause.

  
Align types| Align types in a clause (for example, `serial`, `char`, `varchar`, and so on).  
Align defaults| Align DEFAULT constraints.  
Align nullabilities| Align NULL and NOT NULL constraints.  
Collapse when short| Join multiline short code sections. The length of a section that will be collapsed is determined automatically by IntelliJ IDEA.  
Wrap alter instructions| Move `ALTER` instructions to a new line.  
Align alter instructions| Align all `ALTER` instructions. To use this option, set the Wrap alter instructions option to Do not change.  
  
Item| Description  
---|---  
Wrap CONSTRAINT| Move CONSTRAINT to a new line.  
Wrap KEY/CHECK| Move KEY and `CHECK` to a new line.  
Wrap REFERENCES| Move REFERENCES to a new line.  
Wrap cascade and deferrability| Move CASCADE and DEFERRED constraints to a new line.  
  
Item| Description  
---|---  
Indent content| Add an indent before contents of the `CREATE SCHEMA` statement.  
Minimum blank lines between declaration| Set the minimum number of blank lines between declarations. If you put fewer lines than declared in this option, additional lines are added automatically.  
Maximum blank lines between declaration| Set the maximum number of blank lines between declarations. If you put more lines than declared in this option, additional lines are deleted automatically.  
  
Item| Description  
---|---  
Wrap AS| Move AS clause to a new line.  
Wrap the beginning of the query| Move the beginning of a query to a new line.  
Indent query| Add an indent before a query. The Wrap the beginning of the query option must be enabled.  
  
Item| Description  
---|---  
Wrap first option| Move the first option of the postfix expression to a new line.  
Wrap next option| Move the second option of the postfix expression to a new line.  
Indent options| Add an indent before options of the postfix expression.  
Align options| Align all options of the postfix expression.  
  
27 January 2025

[Queries](code-style-sql-queries.html)[Code](code-style-sql-code.html)
