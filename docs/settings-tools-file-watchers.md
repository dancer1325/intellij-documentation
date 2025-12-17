[//]: # (Source: https://www.jetbrains.com/help/idea/settings-tools-file-watchers.html)
[//]: # (Downloaded: 2025-12-17 20:02:01)

# File Watchers

[Install](managing-plugins.html#install_plugin_from_repo) and enable the File Watchers plugin.

The page is available when the File Watchers plugin is enabled. For more information about configuring File Watchers, refer to [File Watchers](using-file-watchers.html). The File Watchers plugin is not bundled with IntelliJ IDEA, but it can be installed on the Settings | Plugins page, tab Marketplace, as described in [Installing plugins from JetBrains Marketplace](managing-plugins.html#install_plugin_from_repo). 

A File Watcher is an IntelliJ IDEA system that tracks changes to your files and runs a third-party standalone application. IntelliJ IDEA provides predefined File Watcher templates for a number of such standard popular third-party tools ([compilers](http://en.wikipedia.org/wiki/Source-to-source_compiler), compressors, prettifiers, and others).

You can also configure a custom File Watcher to run any other third-party tool.

File Watchers do not start when you open a project in the Safe Mode. For more information, refer to [Project security](project-security.html). 

File Watchers have two dedicated code inspections:

  * The File Watcher available inspection is run in every file where a predefined File Watcher is applicable. If the project has no relevant File Watcher configured, IntelliJ IDEA suggests to add one.

  * The File Watcher problems inspection is invoked by a running File Watcher and highlights errors specific to it.




The page consists of a list of available File Watchers and a toolbar to manage this list.

For each File Watcher, you can decide if it’s going to be available only in the current project (select Project from the Level list) or for all projects (select Global). 

To activate a File Watcher, select the checkbox next to it. When a File Watcher is enabled, it starts automatically as soon as a file of the selected type and in the selected scope is changed or saved, refer to [Configuring advanced options](using-file-watchers.html#ws_filewatcher_advanced_options). If an error occurs while a File Watcher is running, the File Watcher is automatically disabled. To restore the status, enable the File Watcher manually. 

Item| Tooltip and Shortcut| Description  
---|---|---  
![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)| Add `Alt+Insert`| Click this button to open the Choose template popup and select the relevant type of File Watcher. After that IntelliJ IDEA opens the [New Watcher](new-watcher-dialog.html) dialog for customizing the predefined File Watcher according to the settings of the current project.  
![the Edit button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.edit.svg)| Edit `Enter`| Click this button to update the settings of the selected File Watcher in the [Edit Watcher](new-watcher-dialog.html) dialog. The update is applied to the current project File Watcher only, it does not affect the predefined IntelliJ IDEA-level template.  
![the Remove button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)| Remove `Alt+Delete`| Click this button to remove the selected File Watcher. The File Watcher is no longer applied to the files in the current project. Note that this action does not affect the corresponding predefined template which is still available at the IntelliJ IDEA level.  
![the Previous occurrence button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.up.svg) ![the Next occurrence button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.down.svg)| Up `Ctrl+Alt+Up`Down `Ctrl+Alt+Down`| Use these buttons to change the order of File Watcher in the list. This determines the order of launching File Watchers, if more than one are enabled.  
![copy](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.copy.svg)| Copy| Use this button to create a copy of the selected File Watcher.  
![import](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.import.svg)| Import| Click this button to import an existing File Watcher and add it to the list of available File Watchers.  
![export](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.export.svg)| Export| Click this button to export the selected watchers to watchers.xml file, located under the user's home.  
  
08 October 2024

[Web Browsers and Preview](settings-tools-web-browsers.html)[New Watcher Dialog](new-watcher-dialog.html)
