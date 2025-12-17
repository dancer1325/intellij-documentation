[//]: # (Source: https://www.jetbrains.com/help/idea/editing-csv-and-tsv-files.html)
[//]: # (Downloaded: 2025-12-17 19:25:32)

## Extract data

If you need to use the data from the table elsewhere, IntelliJ IDEA provides several possibilities to copy or save it.

IntelliJ IDEA uses data extractors to export data in various formats to a file or the clipboard. Each time you export or copy data, the copied data format is defined by the selected data extractor.

For more information about data extractors, refer to the [corresponding page](data-extractors.html).

If the table data that you need to extract contains commas within the cells, IntelliJ IDEA will honor the contents of such cells.

![Export table data that contains commas within the cells](https://resources.jetbrains.com/help/img/idea/2025.3/db_export_table_data_with_commas_within_cells.png)

### Export data to file or clipboard

  1. To export full data to a file, open a table and click Export Data ![the Export Data icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.download.svg) on the toolbar. Configure export settings and click Export to File.

  2. To export full data to the clipboard, open a table and click Export Data ![the Export Data icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.download.svg) on the toolbar. Configure the export settings and click Export Table to Clipboard.

Alternatively, right-click a cell and select Export Table to Clipboard. The data will be exported using currently selected data extractor.

In contrast to the Export Table to Clipboard action, the Copy `Ctrl+C` action only copies the selection of rows. To copy all the rows, click a cell, press `Ctrl+A` and then `Ctrl+C`. 




### Import data to a database

  1. Click the Import to Database button (![the Import to Database icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.upload.svg)) on the toolbar.

  2. Specify the database, target schema (to create a new table with the exported data) or table (to add exported data to an existing table).

  3. Configure the data mapping and settings for the target table. For more information about the Import dialog, refer to the [Import](import-data.html#import_dialogs) topic.

![Import data to a database](https://resources.jetbrains.com/help/img/idea/2025.3/import_dsv_file_data_to_a_database.png)


