[//]: # (Source: https://www.jetbrains.com/help/idea/settings-tools-database-data-views.html)
[//]: # (Downloaded: 2025-12-17 20:01:51)

## Limitations

Option| Description  
---|---  
Limit page size to| Number of table rows that are shown on one page. If you do not want to limit the number of rows displayed simultaneously, clear the checkbox.Also, you can change the page size by clicking the Change page size list of the pagination toolbar.Consider the following example where Limit page size to is set to 2:![Limit page size to](https://resources.jetbrains.com/help/img/idea/2025.3/PageSize2.png)  
Result set prefetch size| Number of rows from a database that is retrieved in one chunk.A bigger number means less round trips between IDE and a database but more memory for storing a chunk.  
Filter history size| Number of recently-used filtering conditions that are saved for a table in a data editor. Consider the following example where Filter history size is set to 2. The filter history box contains only two conditions.To open the filter history in the editor, click the WHERE or ORDER BY field and press `Alt+Down`.![Filter history size](https://resources.jetbrains.com/help/img/idea/2025.3/DBFilterHistorySize2.png)  
Maximum number of bytes loaded per value| Maximum size of a binary large object to be loaded in bytes.  
Show first N data rows in preview| Limit number of rows for a quick documentation popup. To see quick documentation, press `Ctrl+Q`.
