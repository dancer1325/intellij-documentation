[//]: # (Source: https://www.jetbrains.com/help/idea/configuring-database-connections.html)
[//]: # (Downloaded: 2025-12-17 19:21:45)

## Connection options

### Set a time zone for a connection

  1. Open data source properties by doing one of the following:

     * On the Database tool window toolbar, click ![The Data Sources icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.manageDataSources.svg) Data Sources.

     * Press `Shift+Enter`.

![Open the Data Source and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/open_data_sources_and_drivers_dialog.png)
  2. Select a data source that you want to modify and click the Options tab.

  3. In the Time zone field, start typing the time zone that you want to use.

  4. Apply settings and click OK.

![Select a time zone in the Time zone field](https://resources.jetbrains.com/help/img/idea/2025.3/db_set_time_zone.png)



### Keep the connection alive

You can keep the connection to a database alive by running a keep-alive query after the specified period. You can define the custom query in the driver settings for unsupported databases.

  1. Open data source properties by doing one of the following:

     * On the Database tool window toolbar, click ![The Data Sources icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.manageDataSources.svg) Data Sources.

     * Press `Shift+Enter`.

![Open the Data Source and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/open_data_sources_and_drivers_dialog.png)
  2. On the Data Sources tab, select a data source that you want to modify.

  3. On the Options tab, select the Run keep-alive query each checkbox and type a number of seconds after which IntelliJ IDEA must run a keep-alive query again.




To set a custom keep-alive query for a driver, select the necessary driver on the Drivers tab. Click the Options tab. In the Keep-alive query field, specify the query that you want to use as a keep-alive query.

### Disconnect from a database in a specified period

You can specify a period in seconds after which IntelliJ IDEA terminates the connection.

  1. Open data source properties by doing one of the following:

     * On the Database tool window toolbar, click ![The Data Sources icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.manageDataSources.svg) Data Sources.

     * Press `Shift+Enter`.

![Open the Data Source and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/open_data_sources_and_drivers_dialog.png)
  2. On the Data Sources tab, select a data source that you want to modify.

  3. On the Options tab, select the Auto-disconnect after checkbox and type a number of seconds after which IntelliJ IDEA terminates the connection.




### Set a predefined query to run as you establish a connection

  1. Open data source properties by doing one of the following:

     * On the Database tool window toolbar, click ![The Data Sources icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.manageDataSources.svg) Data Sources.

     * Press `Shift+Enter`.

![Open the Data Source and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/open_data_sources_and_drivers_dialog.png)
  2. On the Data Sources tab, select a data source that you want to modify.

  3. On the Options tab, in the Startup script field, specify the query that you plan to run on a connection to a database.

![Run a predefined query as you establish a connection](https://resources.jetbrains.com/help/img/idea/2025.3/db_specify_startup_script.png)



### Refresh the database state

If someone changed the remote database data or view, the local view of the database might differ from the actual state of the database.

  1. Open data source properties by doing one of the following:

     * On the Database tool window toolbar, click ![The Data Sources icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.manageDataSources.svg) Data Sources.

     * Press `Shift+Enter`.

![Open the Data Source and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/open_data_sources_and_drivers_dialog.png)
  2. On the Data Sources tab, select a data source that you want to modify.

  3. On the Options tab, select the Auto sync checkbox.

If the Auto sync checkbox is cleared, the view of the data source in the Database tool window is synchronized with the actual state of the database only when you click the Refresh icon (![the Refresh button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.refresh.svg)) in the toolbar or press `Ctrl+F5`.

![Refresh the database state](https://resources.jetbrains.com/help/img/idea/2025.3/db_syncronize_database_state.png)



### Filter objects with the object filter

  1. Open data source properties by doing one of the following:

     * On the Database tool window toolbar, click ![The Data Sources icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.manageDataSources.svg) Data Sources.

     * Press `Shift+Enter`.

![Open the Data Source and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/open_data_sources_and_drivers_dialog.png)
  2. On the Data Sources tab, select a data source that you want to modify.

  3. On the Schemas tab, type filtering options in the Object filter field.

Use the following pattern when you compose an expression for the Object filter field.

`<type>:[-]<pattern>`, where:

     * `<type>` might be an aggregate, collation, event, fdw, ftable, mview, operator, package, role, routine, sequence, synonym, table, user, view, vtable.

     * `<pattern>` is a regular expression. To exclude an item, prepend with `-` (minus). For more information about regular expressions, refer to [Class Patterns](https://docs.oracle.com/javase/1.5.0/docs/api/java/util/regex/Pattern.html) at JavaTM 2 Platform Standard Edition 5.0 API Specification.

Also, you can check [the following video at youtube.com](https://www.youtube.com/watch?v=U5SOD-eeK50&t=178s) that describes how to hide objects that you do not need by using the object filter.

![The Object Filter field in data source options](https://resources.jetbrains.com/help/img/idea/2025.3/db_data_source_options_filter.png)



### Filter databases and schemas

  1. Open data source properties by doing one of the following:

     * On the Database tool window toolbar, click ![The Data Sources icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.manageDataSources.svg) Data Sources.

     * Press `Shift+Enter`.

![Open the Data Source and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/open_data_sources_and_drivers_dialog.png)
  2. On the Data Sources tab, select a data source that you want to modify.

  3. On the Schemas tab, type filtering options in the Schema pattern field.

     * `@`: the current database or schema.

     * `*`: every database or schema. You can list schemas after `*:`.

Consider the following examples:

     * `*:*`: all schemas in all databases.

     * `@:*`: all schemas from the current database

     * `@:@`: only the current schema

     * `*:dbo|@:@|db1:s1,s2,s3`: the `dbo` schema from all databases, the current schema, schemas `s1,s2,s3` from the `db1` database.



