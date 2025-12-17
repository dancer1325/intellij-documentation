[//]: # (Source: https://www.jetbrains.com/help/idea/rows.html)
[//]: # (Downloaded: 2025-12-17 19:57:48)

## Manipulating rows

### Add a row

  1. Click ![The Add New Row icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.add_dark.svg) Add Row on the toolbar. Alternatively, right-click the table and select Add Row from the context menu.

  2. Press `Alt+Insert`.

  3. Make your changes.

  4. [(Optional) Submit and commit your changes to the database.](#submit_and_commit_your_changes_to_the_database)




Note that the context menu Clone Row command `Ctrl+D` can be used as an alternative.

### Delete a row

  1. Select a row or rows.

To select multiple rows, click numbers in the gutter. Also, you can press `Ctrl` and click the necessary rows.

  2. Click ![the Delete Row icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.remove_dark.svg) Delete Row on the toolbar. Alternatively, press `Ctrl+Y` or `Delete`.

  3. [(Optional) Submit and commit your changes to the database.](#submit_and_commit_your_changes_to_the_database)




### Remove all rows in a table

  * Right-click a table and navigate to Object Actions | Truncate….

![Remove all rows in a table](https://resources.jetbrains.com/help/img/idea/2025.3/remove_all_rows_of_table.png)



### Clone rows

  1. You can clone a selected row. The copy of the row is added to the end of the table.

To clone a row, right-click the row and select Clone Row. Alternatively, select the row and press `Ctrl+D`.

![Clone a row](https://resources.jetbrains.com/help/img/idea/2025.3/db_clone_row.png)
  2. Make your changes.

  3. [(Optional) Submit and commit your changes to the database.](#submit_and_commit_your_changes_to_the_database)




### Paste CSV lines

In IntelliJ IDEA, you can directly paste multiple CSV lines into a table. The original lines will be split into columns in accordance with the commas. The content of CSV lines will replace that of table rows. If the table does not contain enough rows, new ones will be created.

  1. Select the rows that you want to paste your CSV lines into.

Alternatively, select the table row that you want to paste the first line of your CSV lines into.

  2. Press `Ctrl+V`. Alternatively, select Paste in the context menu.

  3. [(Optional) Submit and commit your changes to the database.](#submit_and_commit_your_changes_to_the_database)




### Submit and commit your changes to the database

Depending on the current [transaction mode](configuring-database-connections.html#transaction-mode), you can submit and commit your changes to the database by doing one of the following:

  1. Tx:Auto mode: click ![The Submit button](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.submitDB.svg) Submit on the toolbar. The changes will be committed to the database automatically.

  2. Tx:Manual mode: click ![The Submit button](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.submitDB.svg) Submit to submit your changes and ![The Commit button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.commit.svg) Submit and Commit to commit the submitted changes to the database.




For more information about committing changes to the database, refer to the [Submit changes to a database](submitting-and-reverting-changes.html) topic.
