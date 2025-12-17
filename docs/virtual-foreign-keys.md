[//]: # (Source: https://www.jetbrains.com/help/idea/virtual-foreign-keys.html)
[//]: # (Downloaded: 2025-12-17 20:06:35)

## Create a virtual foreign key

  1. In the Database tool window, expand the data source tree until the nodes of tables. 

  2. Right-click the table node and select New | Virtual Foreign Key.

  3. In the Modify dialog that opens, enter the name of your virtual foreign key in the Name field.

  4. In the Target Table pane, specify the name of the target table.

  5. In the Columns pane, click the Add button (![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)).

  6. In the Column Name field, specify the name of the column in the child table.

  7. In the Target Name field, specify the name of the column in the target table.

  8. Click OK to add your virtual foreign key.

  9. If the Save external data for <data_source_name> dialog opens, specify the directory for external-data-<data_source_name>.xml file and click Save.


![Create a virtual foreign key in the Modify dialog](https://resources.jetbrains.com/help/img/idea/2025.3/db_create_virtual_foreing_key_in_modify_dialog.png)

  1. Click the table relation in the `ON` clause and press `Alt+Enter`.

  2. Select Store table relation.

  3. If the Save external data for <data_source_name> dialog opens, specify the directory for external-data-<data_source_name>.xml file and click Save.


![Store table relation](https://resources.jetbrains.com/help/img/idea/2025.3/db_store_table_relation.png)
