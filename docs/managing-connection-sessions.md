[//]: # (Source: https://www.jetbrains.com/help/idea/managing-connection-sessions.html)
[//]: # (Downloaded: 2025-12-17 19:31:48)

## New session

Depending on the way you create a new session, it can be connected either automatically or after a certain action. The green dot in the corner of a session's icon indicates the connected status.

You can create a new session by doing either of the following:

  * Open a [query file](query-files.html), view database object's data in data editor, or attach an SQL file to a data source.

As a result, under the data source node in the Services tool window, the new session node appears with a client node under it.

    1. For a query file, the session will be connected once you perform an action that requires interaction with the database. For example, once you [run a query](run-a-query.html#run_statements_in_a_query_console).

    2. For a table, the session is connected automatically, as IntelliJ IDEA requires an active connection to request the table data from the database, receive it, and display it in the data editor.

    3. For an SQL file, the session is connected automatically. To run queries against either of the data source databases or schemas, you have to attach your file to them by selecting them in the <schema> list.

  * Perform an action that requires interaction with the database. For example, [run a stored procedure](run-a-query.html) or run a script by using [run configurations](run-debug-configuration.html).

As a result, the new connected session node appears under the data source node in the Services tool window.



