[//]: # (Source: https://www.jetbrains.com/help/idea/query-execution-plan.html)
[//]: # (Downloaded: 2025-12-17 19:56:36)

# Query execution plan

The `EXPLAIN` command shows the execution plan of a statement. It means you can see details on the approach that the planner took to execute the statement. For example, how the tables are scanned, what join algorithms are used to bring together the required rows, statement execution costs, and other information.

Execution cost is the planner's guess at how long it takes to run the statement. The measurement is made in relative cost units. The execution cost has two options: start-up and total. The start-up cost shows how long it takes before the first row can be processed, while the total cost shows how long it takes to process all the rows.

IntelliJ IDEA supports two types of execution plans:

  * Explain Plan: the result is shown in a mixed tree and table format on a dedicated Plan tab.

  * Explain Plan (Raw): the result is shown in a table format.




If you use the `ANALYZE` option with `EXPLAIN`, the statement is actually executed, not only planned. In this case, you can see the run time statistics in milliseconds.

### Visualize a query plan

  1. Right-click an SQL statement, and select ![the Explain plan icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.consoleShowPlan.svg) Explain Plan | Explain Plan.

Alternatively, click ![the Explain plan icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.consoleShowPlan.svg) Explain Plan on the toolbar and select Explain Plan

  2. By default, you see the tree representation of the query in the Plan tab of the Services tool window. To visualize the query execution plan, click ![the Show Daigram icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.fileTypes.diagram.svg) Show Diagram, or press `Ctrl+Alt+Shift+U`. 




### Generate a flame graph for EXPLAIN

  1. Right-click an SQL statement, and select ![the Explain plan icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.consoleShowPlan.svg) Explain Plan | Explain Plan.

Alternatively, click ![the Explain plan icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.consoleShowPlan.svg) Explain Plan on the toolbar and select Explain Plan

  2. By default, you see the tree representation of the query in the Plan tab of the Services tool window. Click ![the Flame Graph icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.sqlGroupByType.svg) Flame Graph and select between the following options: 

     * Total Cost: how long it takes to return all the rows

     * Startup Cost: how long it takes before the first row can be processed.




### Generate a flame graph for EXPLAIN ANALYSE

  1. Right-click an SQL statement, and select ![the Explain plan icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.consoleShowPlan.svg) Explain Plan | Explain Analyse.

Alternatively, click ![the Explain plan icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.consoleShowPlan.svg) Explain Plan on the toolbar and select Explain Analyse

  2. By default, you see the tree representation of the query in the Plan tab of the Services tool window. Click ![the Flame Graph icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.sqlGroupByType.svg) Flame Graph and select between the following options: 

     * Total Cost: how long it takes to return all the rows (in relative cost units).

     * Actual Total Time: how long it takes to return all the rows (in milliseconds).

     * Startup Cost: how long it takes before the first row can be processed (in relative cost units).

     * Actual Startup Time: how long it takes before the first row can be processed (in milliseconds).




28 October 2025

[Query results](viewing-query-results.html)[SQL for MongoDB](sql-for-mongodb.html)
