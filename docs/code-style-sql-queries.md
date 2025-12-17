[//]: # (Source: https://www.jetbrains.com/help/idea/code-style-sql-queries.html)
[//]: # (Downloaded: 2025-12-17 19:20:41)

## Common

Item| Description  
---|---  
Align the first word of clause| Align keywords to the left or right margin of the first word of a statement section (for example, `SELECT`). The To left with indent option aligns all keywords except for `WITH`, `UNION`, and `INTERSECT` along the left margin with the indent.

  * To left![To left](https://resources.jetbrains.com/help/img/idea/2025.3/sql_formatter_align_first_clause_to_left.png)
  * To left with indent![To left with indent](https://resources.jetbrains.com/help/img/idea/2025.3/sql_formatter_align_first_clause_to_left_with_indent.png)
  * To right![To right](https://resources.jetbrains.com/help/img/idea/2025.3/sql_formatter_align_first_clause_to_right.png)

  
Place clause elements on| Move clause elements to a new line (New line) or leave them on the same line (Same line).  
Place comma| Move a comma (`,`) to the beginning (To begin) or to the end (To end) of a code line.The Auto option analyzes the surrounding context and calculates the most suitable place for a comma. For example, you have three occurrences of a comma: two commas go at the beginning, one comma is at the end. The Auto option will move the third occurrence of the comma to the beginning. This option works only if you have more than three cases in a single context. Otherwise, commas are left as is.If you want to disable a new line after the comma when the To begin option is enabled, clear the Line breaks checkbox on the Wrapping tab.  
Collapse short statements| Join multiline short statements. The length of a statement that will be collapsed is determined automatically by IntelliJ IDEA. To enable this option only for subqueries, select Subqueries only.  
Keep section elements under section header| Move all section elements under the section main keyword (a header).  
Align section elements| Align elements of a clause section.

  * Enabled![Align section elements is on](https://resources.jetbrains.com/help/img/idea/2025.3/sql_formatter_align_section_elements_on.png)
  * Disabled![Align section elements is off](https://resources.jetbrains.com/help/img/idea/2025.3/sql_formatter_align_section_elements_off.png)

  
Align line comments at right of elements| Align line comments that are on the right side of code.
