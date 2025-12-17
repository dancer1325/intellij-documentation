[//]: # (Source: https://www.jetbrains.com/help/idea/foreign-keys.html)
[//]: # (Downloaded: 2025-12-17 19:27:12)

## Productivity tips

### Modify templates for generated index and key names

When you create indexes, and primary and foreign key constraints, their default names are generated according to corresponding templates. For a primary key, for example, the template is `{table}_{columns}_pk`.

  * To view and modify these templates, open the settings `Ctrl+Alt+S` and navigate to Editor | Code Style | SQL | General. Click the Code Generation tab.

The templates can contain variables and text. When you generate a name, the specified text is reproduced literally. For example, when you apply the `{table}_pk` template in the `actor` table, the generated name of the primary key will be `actor_pk`.

To see information about variables and their usage, click a field and press `Ctrl+Q`.

`{unique?u:}` checks if the index is unique and inserts the corresponding sequence of characters. If the index is unique, the template generates a name with the sequence of characters specified between `?` and `:`. For the `{unique?u:}` template, it is `u`. If the index is not unique, the sequence between `:` and `}` is inserted. For the `{unique?u:}` template, it is nothing.

**Example**

You have the `persons` table with columns `FirstName` and `LastName`. The `{table}_{columns}_{unique?u:}index` template generates the following name for the not unique index: `persons_FirstName_LastName_index`.

![Modify templates          for generated index and key names](https://resources.jetbrains.com/help/img/idea/2025.3/db_modify_templates_for_indexes_and_keys.png)



### Navigate between related rows

  * Right-click a row or cell in a table and select Go To | Related Rows.

Alternatively, select a cell and click ![the Related Rows icon](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.goToTable.svg) Related Rows on the quick actions popup toolbar that appears.

![Referenced and referencing data](https://resources.jetbrains.com/help/img/idea/2025.3/db_referencing_referenced_data.png)

In the data editor, you can select several values and navigate to the related data.

For more information about the action behavior options, refer to [Advanced Settings](advanced-settings.html#related_rows_action_behavior).

Also, you can watch [the Navigate by foreign keys video at youtube.com](https://www.youtube.com/watch?v=U5SOD-eeK50&t=1052s) for another example.



