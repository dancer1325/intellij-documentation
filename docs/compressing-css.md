[//]: # (Source: https://www.jetbrains.com/help/idea/compressing-css.html)
[//]: # (Downloaded: 2025-12-17 19:21:30)

## Example: Compressing CSS with CSSO

To minify your code automatically, you need to install CSSO and configure a [CSSO File Watcher](#ws_css_compress_create_file_watcher) which will track changes to your files and run the tool. 

By default, minification starts as soon as a CSS file in the File Watcher's scope is changed and saved. You can specify other [events that invoke CSSO](using-file-watchers.html#launchFileWatcher). Learn more from [File Watchers](using-file-watchers.html).

The generated minified code is stored in a separate file with the name of the source CSS file and the extension min.css. The location of this generated file is defined in the Output paths to refresh field of the [New Watcher dialog](new-watcher-dialog.html). However, in the Project Tree, the file with the minified code is shown under the source CSS file which is displayed as a node. To change this default presentation, [configure file nesting](file-nesting-dialog.html) in the Project tool window `Alt+1`.

### Before you start

  1. Make sure you have [Node.js](http://nodejs.org/) on your computer. 

  2. Make sure the CSS plugin are enabled in the settings. Press `Ctrl+Alt+S` to open settings and then select Plugins. Click the Installed tab. In the search field, type CSS. For more information about plugins, refer to [Managing plugins](managing-plugins.html). 

  3. Install and enable the File Watchers plugin on the Settings | Plugins page, tab Marketplace, as described in [Installing plugins from JetBrains Marketplace](managing-plugins.html#install_plugin_from_repo). 




### Install csso-cli globally

  * In the embedded Terminal (`Alt+F12`) , type:

`npm install -g csso-cli`




### Create a CSSO File Watcher

  1. In the Settings dialog (`Ctrl+Alt+S`) , click File Watchers under Tools. The [File Watchers page](settings-tools-file-watchers.html) that opens shows the list of already configured File Watchers. 

  2. Click ![Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) or press `Alt+Insert` and select the CSSO CSS Optimizer predefined template from the list.

![Create CSSO watcher: Click Add and select template](https://resources.jetbrains.com/help/img/idea/2025.3/ws_css_minification_create_csso_file_watcher_add_watcher.png)

The New Watcher dialog opens.

  3. In the Program field, specify the location of the `csso` executable file.

If you installed `csso-cli` through the Node Package Manager, IntelliJ IDEA locates the package itself and fills in the field automatically with the `csso` alias Otherwise, type the path manually or click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.openDiskHover.svg) and select the file location in the dialog that opens.

  4. Accept the default File Watcher settings or reconfigure them, if necessary, as described in [File Watchers](using-file-watchers.html).

In this example, the default values are as follows:

     * `-i $FileName$ -o $FileNameWithoutExtension$.min.css` in the Arguments field.

     * `$FileNameWithoutExtension$.min.css` in the Output paths to refresh field.

     * `$FileDir$` in the Working directory field.

![Create CSSO watcher: New Watcher dialog with default settings](https://resources.jetbrains.com/help/img/idea/2025.3/ws_css_minification_create_csso_file_watcher_new_watcher_dialog.png)

Click OK to get back to the File Watchers page where the new File Watcher is added to the list:

![Create CSSO watcher: New Watcher added to the list](https://resources.jetbrains.com/help/img/idea/2025.3/ws_css_minification_create_csso_file_watcher_new_watcher_added.png)
  5. Make sure the Enabled checkbox is selected.

By default, the File Watcher will be available in the current project. To use it in other projects, select Global from the Level list.



