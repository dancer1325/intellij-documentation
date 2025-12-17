[//]: # (Source: https://www.jetbrains.com/help/idea/introspection.html)
[//]: # (Downloaded: 2025-12-17 19:30:02)

## Introspection

Introspection is a process of loading metadata of a database. When you perform introspection, structural information in the data source is inspected to detect tables, columns, routines, and other database objects with their attributes.

Introspection is only supported for the databases that have data structure and catalogs.

By default, only the schemas and databases selected to be shown in the Database tool window are introspected.

You can select which schemas and databases will be introspected and shown by either selecting them in the Database tool window, or editing the data source properties in Data Sources and Drivers dialog ( `Shift+Enter`) dialog.

### Select schemas and databases for introspection

Depending on the database size, introspection and loaded metadata can take a significant amount of time and disk space.

  * In Database tool window:

    1. To open Database tool window, select View | Tool Windows | Database from the main menu. Alternatively, press `⌘ 1`.

    2. In Database tool window, click the N of M button next to the data source, database, or schema name.

![Select schemas or databases in Database tool window](https://resources.jetbrains.com/help/img/idea/2025.3/select_schemas_or_databases_to_show.png)
    3. In the schema selection popup window, select the databases or schemas and press `Enter`.

  * In Data Sources and Drivers dialog:

    1. To open the dialog, right-click the data source in Database tool window and select ![the Properties icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.manageDataSources.svg) Properties. Alternatively, click the ![the Settings button](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.manageDataSources_dark.svg) Data Source Properties icon on toolbar.

    2. In the Schemas tab of Data Sources and Drivers dialog, select the databases or schemas.

![Select schemas or databases in data source properties](https://resources.jetbrains.com/help/img/idea/2025.3/db_schemas_or_databases_to_show_in_properties.png)

Note that the Object filter field only defines which objects are visible in Database tool window and does not affect the introspection scope. 

    3. Apply your changes and close the dialog.




Once the necessary databases and schemas are introspected, IDE can resolve the database objects in your scripts to the correct context. The example below demonstrates database object resolve for introspected and not introspected schemas.

![Database objects resolve for the introspected and not introspected schemas](https://resources.jetbrains.com/help/img/idea/2025.3/introspection_objects_resolve.png)

  1. `MySQL` data source that has not been introspected.

  2. The only introspected `guest` database of the `PostgreSQL` data source. The database includes four schemas and only the `public` one has been introspected.

  3. Database object resolve in a query file: successful for the introspected `guest` schema and unsuccessful for the `tests` schema that has not been introspected.




For query files, database object resolve also depends on the selected resolve mode. For more information about query file resolve modes, refer to the [Run queries](run-a-query.html#resolve_modes) topic.

For every data source, you can also select the category of schemas that source code of database objects is loaded for.

### Load sources of database objects for different schemas

  1. To select schemas for which sources of database objects are loaded, open the Data Sources and Drivers dialog ( `Shift+Enter`) and select a data source.

  2. In the Options tab, navigate to the Load sources for setting and select the category of schemas.

  3. Apply the changes and close the dialog.


![Select the category of schemas that database object sources are loaded for](https://resources.jetbrains.com/help/img/idea/2025.3/db_introspection_settings_load_sources_for.png)

Database users might experience a long introspection time if all the objects are being processed, whereas it is usually not required for daily work and coding assistance. To reduce the number of introspected objects, IntelliJ IDEA has additional [introspection types](#introspection_types) and also three [introspection levels](introspection-levels.html) implemented for some of the supported databases.
