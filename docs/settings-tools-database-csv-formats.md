[//]: # (Source: https://www.jetbrains.com/help/idea/settings-tools-database-csv-formats.html)
[//]: # (Downloaded: 2025-12-17 20:01:50)

# CSV Formats

This dialog contains the settings for converting table data into delimiter-separated values formats (for example, CSV, TSV) and vice versa.

This conversion is used to do the following:

  * [View and edit the contents of DSV files as tables.](editing-csv-and-tsv-files.html#open_data_editor)

  * [Export the data to clipboard or to files.](export-data.html#methods-for-exporting-data)

  * [Copy or view the data in data editor.](import-data.html#import_csv)


![The CSV Formats menu of the Database settings](https://resources.jetbrains.com/help/img/idea/2025.3/settings_database_csv_formats.png)

Preview is limited with 10 records to prevent the rest of the data from loading. When you change settings, the preview changes correspondingly.

Item| Description  
---|---  
Formats| Select a template that successfully converts the file data into a table. You can change settings of predefined templates or add a new template. To add a template, click Add Format button (![the Add Format icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg)).Use the Add Format (![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg)), Remove Format (![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)), Up (![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.up.svg)) and Down (![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.down.svg)) buttons to create, delete and reorder the formats; Copy Format (![the Copy Format icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.copy.svg)) to create a copy of the selected format.  
Value separator| Select or type the character that you want to use as a separator for values.  
Row separator| Select or type the character that you want to use as a separator for rows.  
Null value text| Select or type the text that you want to use if a cell contains the `NULL` value.  
Add row prefix/suffix| Click the link and type a row prefix and suffix. Prefix and suffix are character sequences which in addition to the row separator indicate the beginning and end of a row.  
Quotation| Each line in the area under Quotation is a quotation pattern. A quotation pattern includes:

  * Left: a quotation character that is inserted before a value.
  * Right: a quotation character that is inserted after a value.
  * Escape: an escape method or character for the cases when the quotation character is part of a value. The <duplicate> value means that if a quotation character occurs within a value, it is doubled. You can specify your own escape character.

If there is more than one pattern, the first pattern is used.Use the Add (![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg)), Remove (![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)), Up (![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.up.svg)) and Down (![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.down.svg)) buttons to create, delete and reorder the patterns.  
Quote values| Select when you want to enclose values within quotation characters.

  * Never: do not quote values.
  * When needed: quote a value if it contains the value or the row separator.
  * Always: quote all the values.

  
Trim whitespaces| Ignore or remove whitespace characters. If this checkbox is cleared, the whitespace characters are treated as parts of the corresponding values.  
First row is header| Treat the first row as a row that contains column names.  
First column is header| Treat the first column as a column that contains row names.  
  
08 October 2024

[Terminal settings](settings-tools-terminal.html)[Database](settings-tools-database.html)
