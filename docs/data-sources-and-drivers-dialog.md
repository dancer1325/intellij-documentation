[//]: # (Source: https://www.jetbrains.com/help/idea/data-sources-and-drivers-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:24:00)

## Overview

In the Data Sources and Drivers dialog, you can manage your [data sources](managing-data-sources.html#data_sources) and database drivers.

![the Data Sources and Drivers dialog](https://resources.jetbrains.com/help/img/idea/2025.3/data_sources_and_drivers_dialog.png)

A driver is a collection that includes [database driver](https://en.wikipedia.org/wiki/JDBC_driver) files and default settings for creating a data source.

### Left pane controls

When you select an item from the list of data sources and drivers, settings of the item appear on the right side of the dialog.

#### Toolbar

Item| Shortcut| Description  
---|---|---  
![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)| `Alt+Insert`| Create a data source or a driver.Android SQLite to create a data source for an SQLite database located on an Android device or emulator. An Android application module and Android SDK are required and must be defined in IntelliJ IDEA.For more information, refer to [Android SQLite data source settings](#android).  
![the Remove icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)| `Delete`| Remove the selected item or items from the list.  
![the Duplicate icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.copy.svg)| `Ctrl+D`| Create a copy of the selected data source or driver.  
![the Go to Driver icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg)| `Ctrl+B`| Navigate to the driver settings that are associated with the selected data source.  
![the Make Global icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.export.svg) ![the Move to Project icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.import.svg)| | Move the selected data source to the global or project level.For more information about global and project levels, refer to [Data sources](managing-data-sources.html).  
![the Back icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.back.svg) ![the Forward icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.forward.svg)| | Switch between recently-used items.  
  
#### Context menu

Item| Shortcut| Description  
---|---|---  
![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) Add| `Alt+Insert`| Create a data source or a driver.

  * Android SQLite to create a data source for an SQLite database located on an Android device or emulator. An Android application module and Android SDK are required and must be defined in IntelliJ IDEA.For more information, refer to [Android SQLite data source settings](#android).

  
![the Remove icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg) Remove| `Delete`| Remove the selected item or items from the list.  
![the Duplicate icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.copy.svg) Duplicate| `Ctrl+D`| Create a copy of the selected data source or driver.  
![the Go to Driver icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) Go to Driver| `Ctrl+B`| Navigate to the driver settings that are associated with the selected data source.  
![the Make Global icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.export.svg) Make Global![the Move to Project icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.import.svg) Move to Project| | Move the selected data source to the global or project level.For more information about global and project levels, refer to [Data sources](managing-data-sources.html).  
Change Driver| | Associate a data source with a driver.  
![the Reset Changes icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.vcs.revert.svg) Reset Changes| `Ctrl+Alt+Z`| Revert changes for the selected item.  
Load Sources| | Load source code of database objects for the selected category of schemas.  
![the Show Driver Usages icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.search.svg) Show Driver Usages| `Alt+F7`| Show data sources that use the selected driver.
