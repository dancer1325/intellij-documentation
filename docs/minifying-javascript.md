[//]: # (Source: https://www.jetbrains.com/help/idea/minifying-javascript.html)
[//]: # (Downloaded: 2025-12-17 19:32:30)

## Example: Compressing JavaScript with terser

To compress your code automatically, you need to install terser and configure a [UglifyJS File Watcher](#ws_minifying_js_create_file_watcher) which will track changes to your files and run the tool. 

By default, minification starts as soon as a JavaScript file in the File Watcher's scope is changed and saved. You can specify other [events that invoke terser](using-file-watchers.html#launchFileWatcher). Learn more from [File Watchers](using-file-watchers.html).

The generated minified code is stored in a separate file with the name of the source JavaScript file and the extension min.js. The location of this generated file is defined in the Output paths to refresh field of the [New Watcher dialog](new-watcher-dialog.html). However, in the Project Tree, the file with the minified code is shown under the source JavaScript file which is displayed as a node. To change this default presentation, [configure file nesting](file-nesting-dialog.html) in the Project tool window `Alt+1`.

### Before you start

  1. Make sure you have [Node.js](http://nodejs.org/) on your computer. 

  2. Make sure the JavaScript and TypeScript bundled plugin is enabled in the settings. Press `Ctrl+Alt+S` to open settings and then select Plugins. Click the Installed tab. In the search field, type JavaScript and TypeScript. For more information about plugins, refer to [Managing plugins](managing-plugins.html). 

  3. Install and enable the File Watchers plugin on the Settings | Plugins page, tab Marketplace, as described in [Installing plugins from JetBrains Marketplace](managing-plugins.html#install_plugin_from_repo). 




### Install terser

  * In the embedded Terminal (`Alt+F12`) , type:

`npm install --save-dev terser`

Learn more from the [npmjs official website](https://www.npmjs.com/package/terser).




### Create a File Watcher

  1. In the Settings dialog (`Ctrl+Alt+S`) , click File Watchers under Tools. The [File Watchers page](settings-tools-file-watchers.html) that opens shows the list of already configured File Watchers. 

  2. Click ![Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) or press `Alt+Insert` and select the UglifyJS predefined template from the list.

![Create UglifyJS \(terser\) watcher: Click Add and select template](https://resources.jetbrains.com/help/img/idea/2025.3/ws_js_minification_create_uglifyjs_file_watcher_add_watcher.png)

The New Watcher dialog opens.

![Create UglifyJS \(terser\) watcher: New Watcher dialog with default settings](https://resources.jetbrains.com/help/img/idea/2025.3/ws_js_minification_create_uglifyjs_file_watcher_new_watcher_dialog.png)
  3. In the Program field, specify the location of the terser executable file. Type the path manually or click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.openDiskHover.svg) and select the file location in the dialog that opens.

  4. By default, the Scope field shows Project Files. To avoid minification of already minified files, configure a custom scope with the `file:*js&&!file:*.min.*` pattern, as described in [Define a new scope](configuring-scopes-and-file-colors.html#creating-a-new-custom-scope).

![Type pattern manually](https://resources.jetbrains.com/help/img/idea/2025.3/ws_add_scope_type_pattern.png)

Then select the new scope from the Scopes list.

![Select custom scope](https://resources.jetbrains.com/help/img/idea/2025.3/ws_js_minification_create_uglifyjs_file_watcher_new_watcher_dialog_select_custom_scope.png)
  5. Accept the other default File Watcher settings or reconfigure them, if necessary, as described in [File Watchers](using-file-watchers.html), and click OK. IntelliJ IDEA brings you back to the File Watchers page where the new File Watcher is added to the list:

![Create UglifyJS watcher: New Watcher added to the list](https://resources.jetbrains.com/help/img/idea/2025.3/ws_js_minification_create_uglifyjs_file_watcher_new_watcher_added.png)
  6. Make sure the Enabled checkbox is selected.

By default, the File Watcher will be available in the current project. To use it in other projects, select Global from the Level list.




### Run terser

IntelliJ IDEA runs terser automatically when you change a JavaScript file from the [selected scope](#ws_js_minify_example_terser_scope).



