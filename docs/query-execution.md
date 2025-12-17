[//]: # (Source: https://www.jetbrains.com/help/idea/query-execution.html)
[//]: # (Downloaded: 2025-12-17 19:56:37)

# Query execution

This topic describes the available settings for a query execution. For more information about working with queries in IntelliJ IDEA, refer to the following topics:

  * [Run queries](run-a-query.html)

  * [Query results](viewing-query-results.html)

  * [Query execution plan](query-execution-plan.html)




Item| Description  
---|---  
When caret inside statement execute| If the caret is inside a statement, perform the following actions:

  * Ask what to execute: display a popup where you can select what part of a statement or statements to execute.![Ask what to execute](https://resources.jetbrains.com/help/img/idea/2025.3/db_query_exec_ask_what_to_execute.png)
  * Smallest subquery or statement: execute the smallest subquery or statement from the script. For example, when the caret is inside a subquery, the whole statement is executed, including a subquery.![Execute the smallest subquery or statement](https://resources.jetbrains.com/help/img/idea/2025.3/db_query_exec_smallest_subquery_or_statement.png)
  * Smallest statement: execute the smallest statement from the script. For example, when the caret is inside a subquery, the subquery is executed.![Execute the smallest statement](https://resources.jetbrains.com/help/img/idea/2025.3/db_query_exec_smallest_statement.png)
  * Largest statement: execute the largest statement from the script. For example, when the caret is inside a subquery, an outer statement is executed.![Execute the largest statement](https://resources.jetbrains.com/help/img/idea/2025.3/db_query_exec_largest_statement.png)
  * Largest statement or batch: execute the largest statement or a batch of statements from the script. For Transact-SQL (SQL Server and Sybase), the current batch of statements is executed. For all other dialects, the same as the previous option.
  * Whole script: execute the whole script.![Execute the whole script](https://resources.jetbrains.com/help/img/idea/2025.3/db_query_exec_whole_script.png)
  * Everything from caret: execute everything below the caret.![Execute everything below the caret](https://resources.jetbrains.com/help/img/idea/2025.3/db_query_exec_everything_below_caret.png)

  
When caret outside statement execute| If the caret is outside a statement (for example, on a blank line or within a comment), perform one of the following actions:

  * Nothing: stop execution.![Nothing is executed](https://resources.jetbrains.com/help/img/idea/2025.3/db_query_exec_out_nothing.png)
  * Whole script: execute the whole script.![The whole script is executed](https://resources.jetbrains.com/help/img/idea/2025.3/db_query_exec_out_whole_script.png)
  * Everything below caret: execute everything below the caret.![Everything below the caret is executed](https://resources.jetbrains.com/help/img/idea/2025.3/db_query_exec_out_everything_below_caret.png)

  
For selection execute| If the code is selected (highlighted), perform one of the following options:

  * Exactly as one statement: execute exactly what is selected as a single statement.For example, consider this code snippet: BEGIN; UPDATE actor SET first_name='John' WHERE actor_id=100; UPDATE actor SET last_name='Doe' WHERE actor_id=100; COMMIT; Executing this code snippet as one statement will ensure that both `UPDATE` commands either succeed or fail together as part of the same transaction. If split into different statements, one could succeed while the other fails, disrupting the data integrity.
  * Exactly as separate statements: execute exactly what is selected. If the selection contains more than one statement, the statements are executed as separate statements.For example, if you want to run several SQL commands at once, and you don't necessarily need them all to succeed or fail together.
  * Smart expand to script: expand a selection to form a sequence of valid statements. For example, if there is at least one statement border within the selection, the selection is expanded to form a sequence of valid statements. This sequence is then executed. Otherwise, execute what is selected.

  
Open results in new tab| You can select to view query results on individual tabs, or on one and the same tab. For the single tab, the tab is updated for each query.

  * Select the checkbox to create a new tab with query results each time you run the `SELECT` query. Using this approach, you can keep results of all the queries that you have run.
  * If the checkbox is cleared, the same tab is used to show query results. Information on the tab is updated to show the result.In this case, when you get the result that you want to keep, you can pin the tab by right-clicking its header and selecting Pin Tab in the context menu.

  
Split a script for execution in Generic and ANSI SQL dialects| Set the query parsing for unsupported databases that use SQL:2016 or Generic dialects. The Generic dialect differs from SQL:2016 in error highlighting. In the Generic dialect, all found errors are not highlighted.

  * Into valid ANSI SQL statements or by separator: IntelliJ IDEA analyzes a script and splits it on valid statements or by separators. This setting is default.
  * Into ANSI SQL statements: split scripts according to the SQL:2016 grammar.
  * By statement separator: extract and run statements by separators. For the Generic dialect, the separator is a semicolon.

  
Review parameters before execution| When you run a statement with parameters, IntelliJ IDEA saves parameter values in memory. Select this checkbox and next time you execute the statement, IntelliJ IDEA will show you the last used parameter values. You can change them before running the statement.Clear this checkbox and IntelliJ IDEA will execute the statement immediately without showing you the parameter values.  
Show warning before running potentially unsafe queries| Select to display warnings for potentially unsafe queries.If you forgot to put the `WHERE` or `WHERE TRUE` clause in `DELETE` and `UPDATE` statements, IntelliJ IDEA displays a notification to remind you about that.![Notification when you type DELETE and UPDATE without WHERE](https://resources.jetbrains.com/help/img/idea/2025.3/db_update_delete_notification.png)When you run the statements, IntelliJ IDEA shows you the warning. If you omitted the `WHERE` or `WHERE TRUE` clause intentionally, you can execute current statements as you planned by clicking Execute in the warning.![Warning when you run DELETE and UPDATE without WHERE](https://resources.jetbrains.com/help/img/idea/2025.3/db_update_delete_warning.png)  
  
01 December 2025

[Database](settings-tools-database.html)[Output and Results](output-and-results.html)
