[//]: # (Source: https://www.jetbrains.com/help/idea/running-and-debugging-typescript.html)
[//]: # (Downloaded: 2025-12-17 19:59:17)

## Run and debug server-side TypeScript

With IntelliJ IDEA, you can run and debug server-side TypeScript code without previously compiling it into JavaScript.

For running and debugging of server-side multiple TypeScript file applications IntelliJ IDEA uses a built-in loader. When running or debugging a single file, you can turn the loader off by selecting None from the TypeScript loader list in the run/debug configuration.

### Before you start

  1. Make sure you have [Node.js](http://nodejs.org/) 18 or higher on your computer. 

  2. Make sure the Node.js plugin is enabled in the settings. Press `Ctrl+Alt+S` to open settings and then select Plugins. Click the Installed tab. In the search field, type Node.js. For more information about plugins, refer to [Managing plugins](managing-plugins.html). 




### Run server-side TypeScript code

You can run server-side TypeScript from the Project tool window `Alt+1`, from the editor, or from the Run widget. 

  * In the Project tool window `Alt+1`, right-click the TypeScript file to run or the starting file of your application and select Run <TypeScript file name> from the context menu.


![Run server-side TypeScript from the Project tool window](https://resources.jetbrains.com/help/img/idea/2025.3/ws_ts_run_single_file_project_tw.png)

  * In the editor, open the TypeScript file to run or the starting file of your application and select Run <TypeScript file name> from the list.


![Run server-side TypeScript from the editor](https://resources.jetbrains.com/help/img/idea/2025.3/ws_ts_run_single_file_editor.png)

  * In the editor, open the TypeScript file to run or the starting file of your application. Then from the Run widget on the toolbar select Current file and click ![the Run icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.run.run.svg) next to it.

Alternatively, from the Run widget select a [previously created run/debug configuration](#ws_ts_server_side_run_generated_rc) and click ![the Run icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.run.run.svg) next to it.


![Run server-side TypeScript from the Run widget](https://resources.jetbrains.com/help/img/idea/2025.3/ws_ts_run_single_file_widget.png)

#### Run TypeScript scratch files

To run a scratch file, besides the above-mentioned methods, you can also click ![the Run icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.run.run.svg) in the gutter and select the required action from the list. 

![Run a TypeScript scratch file](https://resources.jetbrains.com/help/img/idea/2025.3/ws_ts_run_single_file_scratch.png)

#### Auto-generated temporary run/debug configuration

No matter which way to run server-side TypeScript code you might choose, IntelliJ IDEA creates a temporary run/debug configuration of the type Node.js which you can save, edit, and reuse for running and debugging.

![Node.js run/debug configuration for running and debugging server-side TypeScript](https://resources.jetbrains.com/help/img/idea/2025.3/ws_ts_server_side_node_rc.png)

Learn more from [Run/debug configurations](run-debug-configuration.html).

### Debug server-side TypeScript code

You can debug server-side TypeScript from the Project tool window `Alt+1`, from the editor, or from the Run widget. 

  1. Set the [breakpoints](using-breakpoints.html) where necessary.

  2. In the Project tool window, right-click the TypeScript file to debug or the starting file of your application and select Debug <TypeScript file name> from the context menu.


![Run server-side TypeScript from the Project tool window](https://resources.jetbrains.com/help/img/idea/2025.3/ws_ts_debug_single_file_project_tw.png)

  1. Set the [breakpoints](using-breakpoints.html) where necessary.

  2. In the editor, open the TypeScript file to debug or the starting file of your application and select Debug <TypeScript file name> from the context menu.


![Debug server-side TypeScript from the editor](https://resources.jetbrains.com/help/img/idea/2025.3/ws_ts_debug_single_file_editor.png)

  1. Set the [breakpoints](using-breakpoints.html) where necessary.

  2. In the editor, open the TypeScript file to debug or the starting file of your application. Then from the Run widget on the toolbar select Current file and click ![the Debug icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.run.debug.svg) next to it.

Alternatively, from the Run widget select a [previously created run/debug configuration](#ws_ts_server_side_run_generated_rc) and click ![the Debug icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.run.debug.svg) next to it.


![Debug server-side TypeScript from the Run widget](https://resources.jetbrains.com/help/img/idea/2025.3/ws_ts_debug_single_file_widget.png)

#### Debug TypeScript scratch files

To debug a scratch file, besides the above-mentioned methods, you can also click ![the Run icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.run.run.svg) in the gutter and select the required action from the list. 

![Run a TypeScript scratch file](https://resources.jetbrains.com/help/img/idea/2025.3/ws_ts_debug_single_file_scratch.png)

### Use ts-node

If you need to run or debug single TypeScript files with Node.js, you can use [ts-node](https://www.npmjs.com/package/ts-node) instead of compiling your code as described in [Compiling TypeScript into JavaScript](#ws_ts_compile).

### Install ts-node

  * In the embedded Terminal (`Alt+F12`) , type:

`npm install --save-dev ts-node`




### Create a custom Node.js run/debug configuration for ts-node

  1. Go to Run | Edit Configurations. Alternatively, select Edit Configurations from the Run widget on the toolbar. 

![Open the Edit Configurations dialog](https://resources.jetbrains.com/help/img/idea/2025.3/ws_client_ts_run_config_create.png)

In the Edit Configurations dialog that opens, click the Add button (![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)) on the toolbar and select Node.js from the list. The [Run/Debug Configuration: Node.js](run-debug-configuration-node-js.html) dialog opens.

  2. In the Node Parameters field, add `--require ts-node/register`.

  3. Specify the Node.js runtime to use.

If you choose the Project alias, IntelliJ IDEA will automatically use the project default interpreter from the Node runtime field on the [JavaScript Runtime](javascript-runtime.html) page . In most cases, IntelliJ IDEA detects the project default runtime and fills in the field itself.

You can also choose another configured local or remote interpreter or click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and configure a new one.

  4. In the File field, specify the TypeScript file to run or debug. Depending on your workflow, you can do that explicitly or using a [macro](built-in-macros.html).

     * If you are going to always launch the same TypeScript file, click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.open.svg) and select this file in the dialog that opens. By default, the run/debug configuration gets the name of the selected file.

     * If you need to launch different files, type `$FilePathRelativeToProjectRoot$`. With this [macro](built-in-macros.html), IntelliJ IDEA will always launch the file in the active editor tab.

![Custom run-debug configuration for ts-node](https://resources.jetbrains.com/help/img/idea/2025.3/ws_ts_debug_ts_node.png)
  5. If necessary, specify any additional parameters for `ts-node` (for example, `--project tsconfig.json`) in the Application parameters field.

  6. Save the configuration.




### Run server-side TypeScript with ts-node

Depending on the way you specified your TypeScript file in the run/debug configuration, do one of the following:

  * If you typed the filename explicitly, select the required configuration from the Run widget on the toolbar and click ![the Run button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.run.run.svg) next to the list or press `Shift+F10`.

  * If you specified a macro, open the TypeScript file to run in the editor, select the [newly created configuration](#ws_ts_run_debug_directly_create_node_config) from the Run widget on the toolbar, and click ![the Run button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.run.run.svg) or press `Shift+F10`.




IntelliJ IDEA shows the output in the Run tool window.

### Debug server-side TypeScript with ts-node

  1. In the TypeScript file to debug, set the [breakpoints](using-breakpoints.html) as necessary.

  2. Depending on the way you specified your TypeScript file in the run/debug configuration, do one of the following:

     * If you typed the filename explicitly, select the required configuration from the Run widget on the toolbar and click ![the Debug button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.run.debug.svg) or press `Shift+F9`.

     * If you specified a macro, open the TypeScript file to debug in the editor, select the [newly created configuration](#ws_ts_run_debug_directly_create_node_config) from the Run widget and click ![the Debug button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.run.debug.svg) or press `Shift+F9`.



