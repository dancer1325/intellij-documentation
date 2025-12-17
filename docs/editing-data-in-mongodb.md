[//]: # (Source: https://www.jetbrains.com/help/idea/editing-data-in-mongodb.html)
[//]: # (Downloaded: 2025-12-17 19:25:34)

# Editing data in MongoDB

### Modify data in the data editor

  1. Open the MongoDB collection in the data editor.

  2. Double-click the cell and modify a value.

  3. Click ![the Preview pending changes icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.previewChanges.svg) Preview Pending Changes for the DML preview.


![Preview pending changes](https://resources.jetbrains.com/help/img/idea/2025.3/db_mongodb_preview_pending_changes_icon.png)

### Add a document to a collection

For MongoDB, adding a document to a collection is similar to adding a row to a relational table. The difference is that it is not mandatory for all the documents of a collection to have the same fields. 

  1. In the Database tool window, double-click a MongoDB collection to open it in the data editor.

  2. To add the draft of a document, right-click any area in the data editor and select Add Row. Alternatively, click ![The Add Row icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) Add Row on the toolbar.

  3. Change the values of fields from `<unset>` to the required ones.

If a specific field is not required in the new document, or must be generated upon the new document creation (for example, the values of `_id` column), leave it as `<unset>`.

  4. If you need to add the fields that are not currently present as columns in the new document, right-click any area in the data editor and select Add Column. Set the values of your new fields for the new document.

  5. Click ![The Submit icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.submitDB.svg) Submit on the toolbar.


![Add a document to a MongoDB collection](https://resources.jetbrains.com/help/img/idea/2025.3/db_mongodb_add_document_to_collection.png)

### Delete a document from a collection

For MongoDB, deleting a document from a collection is similar to deleting a row from a relational table. 

  1. In the Database tool window, double-click a MongoDB collection to open it in the data editor.

  2. Select the document that you want to delete, right-click it and select Delete Row. Alternatively, click ![The Delete Row icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg) Delete Row on the toolbar.

  3. Click ![The Submit icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.submitDB.svg) Submit on the toolbar.


![Delete a document from a MongoDB collection](https://resources.jetbrains.com/help/img/idea/2025.3/db_mongodb_delete_document_from_collection.png)

### View and edit data in a separate editor

You can view and edit data and also raw JSON in a separate editor.

  * Right-click a cell in the collection opened in the data editor and select Open in Value Editor.

In the separate editor, you can wrap long values and change their types. To wrap a value, click ![the Toggle Soft Wrap icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.softWrap.svg) Toggle Soft-Wrap. To change the type, click the type list and select the necessary value.


[![Modify data in a separate editor](https://resources.jetbrains.com/help/img/idea/2025.3/db_mongodb_modify_data_in_a_separate_editor.png)](https://resources.jetbrains.com/help/img/idea/2025.3/db_mongodb_modify_data_in_a_separate_editor.png)

Alternatively, to change a type, you can right-click a cell and select Change Type.

[![Change the type of value in the data editor](https://resources.jetbrains.com/help/img/idea/2025.3/db_mongodb_change_type.png)](https://resources.jetbrains.com/help/img/idea/2025.3/db_mongodb_change_type.png)

### Add and delete columns

  * Right-click a header row of a column and select Add Column or Delete Column.


![Add and delete column actions in a context menu](https://resources.jetbrains.com/help/img/idea/2025.3/db_mongodb_add_and_delete_operations_for_columns.png)

28 October 2025

[Submit changes to a database](submitting-and-reverting-changes.html)[Export and import](exporting-and-importing-data.html)
