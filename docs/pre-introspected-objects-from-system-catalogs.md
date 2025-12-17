[//]: # (Source: https://www.jetbrains.com/help/idea/pre-introspected-objects-from-system-catalogs.html)
[//]: # (Downloaded: 2025-12-17 19:34:07)

# Pre-introspected objects from system catalogs

A system catalog is a place where a relational database management system (DBMS) stores information about tables and columns, built-in functions, and other schema objects. The IDE uses data from this catalog for code completion and other coding assistance operations.

System schemas have the ![Enable or disable the usage of pre-introspected objects](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.actions.lightning.svg) lightning icon in the schema selection dialog. If you do not select these schemas, IntelliJ IDEA does not introspect them and does not show them in the Database tool window. Though information about schema objects is used in coding assistance. It is possible because IntelliJ IDEA uses the internal data about schema objects that was introspected earlier (pre-introspected data).

To disable usage of pre-introspected data in IntelliJ IDEA, open data source settings by pressing `Shift+Enter`, click the Options tab and deselect Use pre-introspected objects for system catalogs that are not introspected.

Examples of system catalogs in different DBMS:

  * PostgreSQL: `pg_catalog`, `information_schema`

  * Microsoft SQL Server: `INFORMATION_SCHEMA`

  * Oracle: `SYS`, `SYSTEM`

  * MySQL, MariaDB: `information_schema`

  * IBM Db2 LUW: `SYSCAT`, `SYSFUN`, `SYSIBM`, `SYSIBMADM`, `SYSPROC`, `SYSPUBLIC`, `SYSSTAT`, `SYSTOOLS`


![Show objects from system catalogs in coding assistance](https://resources.jetbrains.com/help/img/idea/2025.3/pre_introspected_objects_of_system_catalogs.png)

### Introspect system catalogs for a data source

By default, IntelliJ IDEA uses pre-introspected objects for system catalogs.

  1. In the Database tool window, right-click a data source and select ![the Properties icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.manageDataSources.svg) Properties.

  2. In the Data Sources and Drivers dialog, click the Options tab.

  3. Clear the Use pre-introspected objects for system catalogs that are not introspected checkbox.

![Introspect system catalogs for a data source](https://resources.jetbrains.com/help/img/idea/2025.3/db_introspect_system_catalogs_for_data_source.png)
  4. Click the N of M button near the database name to open the schema selection popup window.

  5. In the schema selection popup window, select system catalogs that you want to introspect. 




IntelliJ IDEA introspects the selected system catalogs.

### Use pre-introspected data for a certain system catalog

You can still use pre-introspected objects for a certain system catalog even if you disable the usage of such objects for a data source in its settings.

  1. In the Database tool window, right-click a data source and select ![the Properties icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.manageDataSources.svg) Properties.

  2. In the Data Sources and Drivers dialog, click the Options tab.

  3. Clear the Use pre-introspected objects for system catalogs that are not introspected checkbox.

![Introspect system catalogs for a data source](https://resources.jetbrains.com/help/img/idea/2025.3/db_introspect_system_catalogs_for_data_source.png)
  4. Click the N of M button near the database name to open the schema selection popup window.

  5. In the schema selection popup window, click the system catalog name. 

  6. Clear the checkbox near system catalog name and click the ![Enable or disable the usage of pre-introspected objects](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.actions.lightning.svg) lightning icon in the upper-right corner of the window.




IntelliJ IDEA uses pre-introspected data only for the system catalog that you selected.

07 April 2025

[Introspection levels](introspection-levels.html)[MongoDB introspection](how-to-fetch-more-fields-for-mongodb-introspection.html)
