[//]: # (Source: https://www.jetbrains.com/help/idea/compare-data.html)
[//]: # (Downloaded: 2025-12-17 19:21:11)

## Controls of the Diff Viewer for contents

In the Diff Viewer for contents, you can use the same sorting functionality that is available in the data editor. For more information about sorting columns, refer to [Sort data](tables-sort.html).

The primary purpose of the Diff Viewer for contents is to show the differences and similarities of data.

To highlight the differences, IntelliJ IDEA uses the following color coding:

Color| Description  
---|---  
![Rows that differ](https://resources.jetbrains.com/help/img/idea/2025.3/db_diff_content_rows_that_differ.png)| Rows that differ.  
![Cells that differ in a column](https://resources.jetbrains.com/help/img/idea/2025.3/db_diff_content_cells_that_differ.png)| Cells that differ in a column.  
![Rows that are considered equal](https://resources.jetbrains.com/help/img/idea/2025.3/db_diff_content_rows_considered_equal.png)| Rows that are considered equal.  
  
### Detect column insertion

When the tables have a different number of columns, extra columns in the table with more columns are ignored. If the Detect column insertion option is on, the most different columns are ignored. In the following picture, the first column in the second table is the most different and so it is ignored. As a result, the second row is shown as containing the same data.

If the option is off, ignored are the last of the columns. On the following picture, the last column in the second table is ignored. So all the rows are shown as containing different data.

### Tolerance

The Tolerance parameter defines how many columns might differ to consider two rows equal. For example, if you set Tolerance to one, rows that differ in one column are considered equal.

![Compare table data tolerance equals to one](https://resources.jetbrains.com/help/img/idea/2025.3/db_compare_table_data_tolerance_one.png)

With tolerance set to zero, such rows are considered different.

![Compare table data tolerance equals to zero](https://resources.jetbrains.com/help/img/idea/2025.3/db_compare_table_data_tolerance_zero.png)

With this setting, you can also check the columns that differ when data in rows is different. Such rows in those columns are highlighted. Increase the Tolerance option if you have different data more than in one row. For example, with Tolerance set to `1`, you can see that between two tables only the `last_name` column differs.

![columns differ when rows contain different data](https://resources.jetbrains.com/help/img/idea/2025.3/db_columns_differ_when_rows_contain_different_data.png)
