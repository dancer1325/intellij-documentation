[//]: # (Source: https://www.jetbrains.com/help/idea/data-loaders.html)
[//]: # (Downloaded: 2025-12-17 19:23:59)

## Custom data loader

You can also create and use your own scripted data loader that you can write in Groovy.

Consider starting your script with the following code line as an example:

// IJ: extensions = json displayName = JSON tableFirstFormat=false 

The keywords are as follows:

  * `extensions`: List of the file extensions the loader works with. Uses `;` as a separator.

  * `displayName`: Name of the custom loader.

  * `tableFirstFormat`: Defines whether the format is [table-first](advanced-settings.html#open_tabular_data_file_as_table). Default: `true`.




In your script, also add a function that receives the following context: path to the file and the `DataConsumer` interface. For example, `loadJson`:

LOADER.load { ctx -> loadJson(ctx.getParameters()["FILE"], ctx.getDataConsumer()) } 

For the `DataConsumer` interface, definition is as follows:

interface DataConsumer { void consumeColumns(String[] names, Class<?>[] types); void consume(Object... row); } 

  * `void consumeColumns(String[] names, Class<?>[] types);`: This method takes in the column names as the `names` array and the corresponding data types for each column as the `types` array.

  * `void consume(Object... row);`: This method takes in the corresponding cell values for each column as `Object`. Each time the `consume` method is called, it processes one complete row from the table.




For the examples of built-in data loader scripts, open the Project tool window and navigate to Scratches and Consoles | Extensions | Database Tools and SQL | data | loaders.
