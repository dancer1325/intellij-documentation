[//]: # (Source: https://www.jetbrains.com/help/idea/matplotlib-support.html)
[//]: # (Downloaded: 2025-12-17 19:32:03)

## Analyze data

### View data structures

  * When viewing variables in the Python Console, you can click View as Array, View as DataFrame, or View as Series links to display the data in the Data View tool window.

![Viewing data frames](https://resources.jetbrains.com/help/img/idea/2025.3/py_dataframe.png)
  * By default, the new table representation is used.

Click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.moreVertical.svg)More Actions and select ![Switch Between Table Representations](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.actions.swapPanels.svg) Switch Between Table Representations to change the table interface.

IntelliJ IDEA will remember your choice and use the selected table representation in the future, except for the data structures from the newly supported libraries (for example, `polars`), which will always be displayed using the new representation.




To view dataframes or series in a tabular form, click Table View in the upper left corner of the output cell.

![View dataframe as a table](https://resources.jetbrains.com/help/img/idea/2025.3/py_table_view.png)

### Work with tables

### Work with columns

  * To open the table search bar, click the table and press `Ctrl+F`.

  * To open the context menu, right-click the column name:

![Copying table headers](https://resources.jetbrains.com/help/img/idea/2025.3/py_copy_column_name.png)
  * To copy the column name to the clipboard, select Copy Column Name.

  * To select the entire column, select Select Column.

  * To hide a column, select Hide Column. Hide Other Columns will hide all columns except the selected one.

  * To display hidden columns, click Show Column List `Ctrl+F12`. The hidden columns are shown strikethrough. Select a column and press `Space` to toggle its visibility. To search through the column list, start typing a column name in the Show Column List window.

  * To assign a language to a column, use Set Highlighting Language. For more information, refer to [Inject a language for a column](columns.html#enabling_coding_assistance_for_column).

  * To toggle and configure cell coloring, click ![](https://resources.jetbrains.com/help/img/idea/2025.3/intellij.grid.core.impl.icons.tableHeatmap.png) Table Coloring Options.

This option is only available when the table is opened in the Data View tool window. To open it, click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.toolwindows.toolWindowDataView.png) Open in Data View in the upper-right corner of the table.

![Configuring table color mapping](https://resources.jetbrains.com/help/img/idea/2025.3/py_table_viewer_coloring.png)



### Sort data

  * To sort the table data based on the column values, right-click the column name and select Ascending or Descending from the ORDER BY section in the context menu.

  * To add another column to sorting, you can either click the column name while pressing `Alt` or select Ascending or Descending from the Add to ORDER BY section in the context menu.

The data will be sorted by selected columns.

Value column cannot be added to sorting if sorting by the index column is active.

State| Description  
---|---  
![No sorting](https://resources.jetbrains.com/help/img/idea/2025.3/py_ds_no_sorting.png)| Indicates that the data is not sorted in this column. The initial state of the sorting marker.  
![Ascending order](https://resources.jetbrains.com/help/img/idea/2025.3/py_ds_ascending_order.png)| The data is sorted in the ascending order.  
![Descending order](https://resources.jetbrains.com/help/img/idea/2025.3/py_ds_descending_order.png)| The data is sorted in the descending order.  
![Sorting level](https://resources.jetbrains.com/help/img/idea/2025.3/py_ds_sorting_level.png)| The number to the right of the marker (1 on the picture) is the sorting level. You can sort by more than one column. In such cases, different columns will have different sorting levels.  
  



### Filter data

  1. Click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.filter.svg) Open Filter View in the upper-right corner of the table.

  2. In the dialog that opens, select the column where you want to apply the filter and specify the filter criteria. 

You can add your existing variables from RunTime or create a new variable right in the Enter value field.

  3. For columns with the `object` data type, filter values should be entered in quotes.

You can use the Wrap with Quotes action to add them automatically.

![Wrap with Quotes](https://resources.jetbrains.com/help/img/idea/2025.3/py_filter_wrap_quotes.png)
  4. If you want to use additional filters, click Add filter and specify the new filter criteria.

  5. Click Apply to filter data.




To remove or duplicate a filter, click ![Additional Filter Actions](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.actions.more.svg)Additional Filter Actions and select the required option from the list.

### Adjust table formatting

  1. Click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.moreVertical.svg)More Actions and select Format Table...

  2. In the dialog that opens, specify the format and click OK. 

![Dialog with the input field for the format](https://resources.jetbrains.com/help/img/idea/2025.3/py_format_table.png)

To apply this format to all tables, select the checkbox Set by default for all tables.




IntelliJ IDEA supports [Python 2 formatting syntax](https://python-reference.readthedocs.io/en/latest/docs/str/formatting.html).

### Use Expression Input

You can use Expression Input to display multidimensional data in a two-dimensional table format.

  1. Click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.moreVertical.svg)More Actions and select Show Expression Input.

  2. Write your expression in the input field that appears on top of the table and press `Enter`.


![Table expression input](https://resources.jetbrains.com/help/img/idea/2025.3/py_expression_input.png)

### View column statistics

By default, column statistics are turned off.

To change the default mode to Compact or Detailed, navigate to Settings | Languages & Frameworks | Tables.

The Compact mode includes only `None Count` statistics:

![Column statistics in a compact mode](https://resources.jetbrains.com/help/img/idea/2025.3/py_compact_statistics.png)

For numeric data, histograms are plotted and shown together with statistics. Hover over the histogram to view detailed information about each bar.

To view detailed column statistics, do one of the following:

  1. Hover over a column name. A popup with column statistics appears.

  2. Click ![](https://resources.jetbrains.com/help/img/idea/2025.3/grid-core.icons.expui.statisticsPanel.svg) Show Column Statistics and select Detailed.

The detailed statistics are shown above the columns.




![Column statistics for non-numeric data](https://resources.jetbrains.com/help/img/idea/2025.3/py_ds_column_stats_non_numeric.png)

Data type
    

Shows the data type the column belongs to

None Count
    

Shows the number of `None` values in the column

Count
    

Shows the total number of items in a column

Distinct
    

Shows the number of unique values

Top
    

Shows the most popular value

Frequency
    

Shows the number of times an element occurs

![Column statistics for numeric data](https://resources.jetbrains.com/help/img/idea/2025.3/py_ds_column_stats_numeric.png)

Data type
    

Shows the data type the column belongs to

None Count
    

Shows the number of `None` values in the column

Count
    

Shows the total number of items in a column

Mean
    

Shows the average number of all values in the column

Std. Deviation
    

Shows the standard deviation value

Min
    

Shows the minimum value in the column

Pctl
    

Shows values for 5th, 25th, 50th( Median) and 95th percentiles

Max
    

Shows the maximum value in the column

Viewing column statistics in table outputs is equivalent to using the `describe()` method for `Series`. For more information, refer to [pandas.Series.describe](https://pandas.pydata.org/docs/reference/api/pandas.Series.describe.html#pandas-series-describe) and [polars.Series.describe](https://pola-rs.github.io/polars/py-polars/html/reference/series/api/polars.Series.describe.html#polars-series-describe).

### Work with charts

To view dataframes or series in a graphical form, click Chart View in the upper left corner of the output cell.

![View data as a chart](https://resources.jetbrains.com/help/img/idea/2025.3/py_jupyter_view_as_chart.png)

The data will be displayed in the form of a chart. You can change the type of chart and configure additional settings.

![Data displayed as a chart](https://resources.jetbrains.com/help/img/idea/2025.3/py_ds_chart_displayed.png)

### Configure charts

  1. Click ![Show series settings](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.settings.svg) Show series settings to change the initial settings of the chart.

  2. Select the chart type and configure the settings. You can choose one of the following chart types:

     * ![](https://resources.jetbrains.com/help/img/idea/2025.3/intellij.charts.icons.chart.chartBar.svg) Bar

     * ![](https://resources.jetbrains.com/help/img/idea/2025.3/intellij.charts.icons.chart.chartPie.svg) Pie

     * ![](https://resources.jetbrains.com/help/img/idea/2025.3/intellij.charts.icons.chart.chartArea.svg) Area

     * ![](https://resources.jetbrains.com/help/img/idea/2025.3/intellij.charts.icons.chart.chartLine.svg) Line

     * ![](https://resources.jetbrains.com/help/img/idea/2025.3/intellij.charts.icons.chart.chartScatter.svg) Scatter

     * ![](https://resources.jetbrains.com/help/img/idea/2025.3/intellij.charts.icons.chart.chartBubble.svg) Bubble

     * ![](https://resources.jetbrains.com/help/img/idea/2025.3/intellij.charts.icons.chart.chartStock.svg) Stock

     * ![](https://resources.jetbrains.com/help/img/idea/2025.3/intellij.charts.icons.chart.chartAreaRange.svg) AreaRange

     * ![](https://resources.jetbrains.com/help/img/idea/2025.3/intellij.charts.icons.chart.chartBar.svg) Histogram

![Change initial settings of the chart](https://resources.jetbrains.com/help/img/idea/2025.3/py_ds_change_chart_settings.png)
  3. Click the Add new series link to add more series to the chart.




### Save a chart as an image

  1. Click ![Export to PNG](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.download.svg) Export to PNG to save the generated chart in the .png format.

  2. Enter the filename and click Save.




### AI-generated charts

You can generate a number of preview-charts for a DataFrame using AI. These previews can then be transformed into notebook cells.

  1. Click ![](https://resources.jetbrains.com/help/img/idea/2025.3/intellij.ml.llm.core.icons.aiAssistantColored.svg)AI Quick Charts in the upper-right corner of the table.

  2. You will see the suggested charts under the table. Click any of them to insert the corresponding visualization code as a notebook cell.


![AI suggested charts](https://resources.jetbrains.com/help/img/idea/2025.3/py_ai_quick_charts.png)
