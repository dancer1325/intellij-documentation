[//]: # (Source: https://www.jetbrains.com/help/idea/export-data.html)
[//]: # (Downloaded: 2025-12-17 19:26:04)

## Export object structure

Data definition language (DDL) defines the structure of a database, including rows, columns, tables, indexes, and other elements. In IntelliJ IDEA, you can generate data definition structure by using shortcuts with predefined settings or by using the SQL Generator and customize the export settings.

### Generate DDL definitions for database objects

  * In the Database tool window, right-click a database object and select SQL Scripts | SQL Generator `Ctrl+Alt+G`.

On the right toolbar, you can find the following controls:

    * ![The copy icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.copy.svg): copy output to the clipboard.

    * ![The Save to File icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.save.svg): save output to a file.

    * ![Run in a console](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.consoleRun.svg): open output in a query file.

![Generate DDL definitions for database objects](https://resources.jetbrains.com/help/img/idea/2025.3/db_sql_generator.png)



The DEFINER clause specifies the security context (access privileges) for the routine execution. In MySQL and MariaDB, select Skip DEFINER clause to skip this clause when you generate DDL for a procedure or a function.

### Change output settings of the SQL Generator

  1. In the Database tool window, right-click a database object (for example, a table) and select SQL Scripts | SQL Generator `Ctrl+Alt+G`.

  2. In the SQL Generator tool window, click the File Output Options icon (![The File Output Options icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.save.svg)).

  3. From the Layout list, select a method that you want to use:

     * File per object by schema: generates a set of SQL files sorted in folders by schemas.

     * File per object by schema and database: generates a set of SQL files sorted in folders by schemas and databases.

     * File per object: generates a set of SQL files.

     * File per object with order: generates a numbered set of SQL files.

     * File per object by schema and type: generates a set of SQL files sorted in folders by schemas and types.

![Change output settings of the SQL Generator](https://resources.jetbrains.com/help/img/idea/2025.3/db_sql_generator_output_settings.png)



### Generate a DDL definition to the query file

  * In the Database tool window, right-click a database object and select SQL Scripts | Generate DDL to Query Console.




### Generate a DDL definition to the clipboard

  * In the Database tool window, right-click a database object and select SQL Scripts | Generate DDL to Clipboard.

If your database stores DDL of the object, you can retrieve DDL from the database by selecting the Request and Copy Original DDL.



