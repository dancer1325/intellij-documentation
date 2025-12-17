[//]: # (Source: https://www.jetbrains.com/help/idea/database-color-settings-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:24:03)

# Database Color Settings dialog

In the [Database tool window](database-tool-window.html) (View | Tool Windows | Database), right-click any object (for example, a table or a data source) and select Tools | Set Color.

Select the [color](#color) and specify how this color should be used (refer to [Shared](#shared) and [Override recursively](#set_recursively)). Use the checkboxes in the Appearance Settings section to enable or disable the database colors in various places in the user interface.

![Database Color Settings dialog](https://resources.jetbrains.com/help/img/idea/2025.3/db_database_color_settings.png)

Item| Description  
---|---  
Color| Click the color that you want to use for the element or elements selected in the Database tool window.If the color that you want is missing, click Custom and specify the color in the dialog that opens.The color which is currently selected is marked with its name.If you don't want to use any color, click [No color](#no_color).  
Shared| Select the checkbox if you want to share the change of color you are about to make with your team. The database color settings are shared through version control. The new color for the selected element or elements will be stored in the following files:

  * .idea/databaseColors.xml or the .ipr file if the checkbox is selected.
  * .idea/workspace.xml or the .iws file if the checkbox is not selected.

The workspace.xml or the .iws file, normally, is not shared through version control while the rest of IntelliJ IDEA configuration files are.For more information about IntelliJ IDEA configuration files and their sharing, refer to [Projects](creating-and-managing-projects.html).  
Override recursively| If the checkbox is selected, the selected color will be applied to the element itself and all its subordinate elements recursively.If the checkbox is not selected, the colors set individually for the subordinate elements won't change.  
Enable database colors| Clear the checkbox to disable the database colors everywhere in the user interface.  
In Database Explorer| Select the checkbox to apply a color to the database node.When this option is on, database nodes have the color that you have selected.![Colors in Database are enabled](https://resources.jetbrains.com/help/img/idea/2025.3/DBColorsDBOn.png)![Colors in Database are disabled](https://resources.jetbrains.com/help/img/idea/2025.3/DBColorsDBOff.png)  
In editor tabs| Select the checkbox to use the database colors for editor tabs.When this option is on, the tabs have the same color as the corresponding data source or table.![Editor colors are enabled](https://resources.jetbrains.com/help/img/idea/2025.3/DBColorsEditorOn.png)![Editor colors are disabled](https://resources.jetbrains.com/help/img/idea/2025.3/DBColorsDBOff.png)  
In console editors and grids| Select the checkbox to use the database colors for the editing area in query files and data editors.When this option is on, the background of the editing area has the same color as the corresponding data source.![Query file and data editor colors are enabled](https://resources.jetbrains.com/help/img/idea/2025.3/DBColorsConsoleEditorsOn.png)![Query file and data editor are disabled](https://resources.jetbrains.com/help/img/idea/2025.3/DBColorsDBOff.png)  
In toolbars| Select the checkbox to use the database colors for the toolbars of query files and data editors.When this option is on, the toolbar background has the same color as the corresponding data source.![Toolbar colors are enabled](https://resources.jetbrains.com/help/img/idea/2025.3/DBColorsToolbarOn.png)![Toolbar colors are disabled](https://resources.jetbrains.com/help/img/idea/2025.3/DBColorsDBOff.png)  
No Color| Reset all color settings for the selected element.  
  
28 October 2025

[Confirm Drop dialog](confirm-drop-dialog.html)[Schema comparison and migration](schema-comparison-and-migration.html)
