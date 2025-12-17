[//]: # (Source: https://www.jetbrains.com/help/idea/settings-appearance-and-behavior-data-editor-and-viewer.html)
[//]: # (Downloaded: 2025-12-17 20:00:24)

# Data Editor and Viewer

The settings on this page define how table data is shown and modified in your [query files](query-files.html), [Hibernate](working-with-the-hibernate-console.html) and [JPA](using-jpa-console.html) consoles, [data editors](data-editor-and-viewer.html), and so on.

Option| Description  
---|---  
Use custom font| Set the dedicated font for your data. The font is applied for query results and data editor, not for query files and your SQL files.![Custom font applied to the displayed data](https://resources.jetbrains.com/help/img/idea/2025.3/db_custom_font_for_data.png)  
Alternate row colors| Select this checkbox to make the table row colors alternate between two kinds of colors.![Alternating row colors](https://resources.jetbrains.com/help/img/idea/2025.3/alternate_row_colors.png)  
Show boolean values as| Set how you want to display boolean values in the data editor. You can select between the following options.

  * Text: boolean values are shown as text. White dots are displayed with the `true` values to help you distinguish them from the `false` ones.![Display boolean values as text](https://resources.jetbrains.com/help/img/idea/2025.3/db_display_boolean_values_as_text.png)There are the following options of editing a boolean value that is shown as text:
    1. Double-click a cell and select a value from the drop-down list.
    2. To toggle the values, select a cell and press `Space`.
    3. To set a certain value, select a cell and type the value's first letter: `f` for `false`, `t` for `true`, `d` for `default`, `n` for `null`, `g` for `generated`, and `c` for `computed`.
  * Checkboxes: boolean values are shown as checkboxes. If the checkbox is selected, the value is `true`. If the checkbox is cleared, the value is `false`.![Display boolean values as checkboxes](https://resources.jetbrains.com/help/img/idea/2025.3/db_display_boolean_values_as_checkboxes.png)

To set NULL or DEFAULT values, right-click a cell and select Set NULL or Set DEFAULT.  
  
09 October 2025

[Notifications](settings-notifications.html)[Quick Lists](settings-quick-lists.html)
