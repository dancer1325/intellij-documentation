[//]: # (Source: https://www.jetbrains.com/help/idea/cannot-find-a-database-object-in-the-database-tree-view.html)
[//]: # (Downloaded: 2025-12-17 19:19:40)

## Collect diagnostic information

Collecting diagnostic information is necessary for resolving problems. It has to be performed prior to following the troubleshooting steps given in this topic.

To profile the introspection and diagnose possible issues, IntelliJ IDEA can generate three files that include information about the following:

  * dataSource.txt: the data source.

  * introspector.txt: a module that was used to load the metadata from the database.

  * model.xml: a part of the database model. 




This information is helpful when introspection works incorrectly.

  1. Right-click a data source and navigate to Diagnostics | Generate Introspector Diagnostic Files.

  2. IntelliJ IDEA will generate three files with the introspector diagnostic info.

![Notification message with a link to introspection diagnostic files](https://resources.jetbrains.com/help/img/idea/2025.3/db_introspection_info_files_location.png)

Click the link in the Diagnostic information collected notification message to navigate to the directory with generated files.


![Introspection diagnostic files in the file browser window](https://resources.jetbrains.com/help/img/idea/2025.3/db_introspection_info_files.png)

The following screenshots show the example output of these three files.

  * dataSource.txt

![Example of the dataSource.txt file](https://resources.jetbrains.com/help/img/idea/2025.3/db_introspection_info_data_source_file.png)
  * introspector.txt

![Example of the introspector.txt file](https://resources.jetbrains.com/help/img/idea/2025.3/db_introspection_info_introspector_file.png)
  * model.xml

![Example of the model.xml file](https://resources.jetbrains.com/help/img/idea/2025.3/db_introspection_info_model_file.png)


