[//]: # (Source: https://www.jetbrains.com/help/idea/databases.html)
[//]: # (Downloaded: 2025-12-17 19:24:08)

## Display databases

When you create a data source, the data source is created with no databases or schemas selected to display. You need to select the ones you plan to work with yourself. 

### Show and hide databases

  * In the Database tool window, right-click a data source and navigate to Tools | Manage Shown Schemas. Select or clear checkboxes of databases that you want to display or hide. Press `Enter`.

  * Click the N of M link near the data source name. In the database and schema selection window, select or clear checkboxes of databases that you want to display or hide. Press `Enter`. 

![Show and hide schemas and databases](https://resources.jetbrains.com/help/img/idea/2025.3/show_and_hide_dbs_schemas.png)



### Use pattern-based filter

To display and introspect all the databases with names that match a regular expression pattern, do the following:

  1. In the Database tool window, click the N of M link near the data source name.

  2. In the databases and schemas selector, click the add pattern button near All databases.

![Pattern-based schema filter](https://resources.jetbrains.com/help/img/idea/2025.3/db_pattern_based_schemas_filter.png)
  3. In the new filtering node, define the regular expression. For the syntax, click regex for databases near the input field. For more information about the syntax, refer to [Summary of regular-expression constructs](#summary_of_regular_expression_constructs).

Press `Enter` to apply the filter in the selector.

![Regular expressions in pattern-based schema filter](https://resources.jetbrains.com/help/img/idea/2025.3/pattern_based_schemas_filter_regexp.png)
  4. Press `Enter` to apply the filter in Database tool window.

The filtering node with filter can be added under any node, including another filtering node.




Multiple patterns combine multiplicities, not intersect them.

The All schemas node behaves differently now: it doesn't select the default schema automatically. You need to select between All schemas, Default schema, or a filtering node.

### Show all the schemas and databases

  * To display all the available databases in the Database tool window (View | Tool Windows | Database), click the Show Options Menu button and select the All Namespaces option.

    * Enabled

![Show All Namespaces is enabled](https://resources.jetbrains.com/help/img/idea/2025.3/show_all_namespaces_enabled.png)
    * Disabled

![Show All Namespaces is disabled](https://resources.jetbrains.com/help/img/idea/2025.3/show_all_namespaces_disabled.png)


