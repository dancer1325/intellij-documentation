[//]: # (Source: https://www.jetbrains.com/help/idea/jscs.html)
[//]: # (Downloaded: 2025-12-17 19:30:42)

# JSCS

Since IntelliJ IDEA 2020.2, JSCS support in the IDE has been deprecated, refer to the [JSCS official website](https://jscs-dev.github.io/) for details.

However, JSCS support is still available through the JSCS plugin, which can be installed on the Settings | Plugins page as described in [Installing plugins from JetBrains Marketplace](managing-plugins.html#install_plugin_from_repo). 

When [JSCS support is enabled](#ws_js_linters_jscs_enable_and_configure), IntelliJ IDEA highlights errors that [JSCS](https://eslint.org/blog/2016/04/welcoming-jscs-to-eslint) detects, provides descriptions for them, and suggests quick-fixes where possible.

Descriptions of the errors detected in the current file and quick-fixes for them are available from the editor and from the File tab of the [Problems](linters.html#ws_js_linters_general_problems_tool_window) tool window.

Errors in all previously opened files and quick-fixes for them are shown in the Project Errors tab of the Problems tool window. To open the tool window, click the Inspection widget in the upper-right corner of the editor:

![Inspection widget](https://resources.jetbrains.com/help/img/idea/2025.3/inspection-widget.png)

For more information, refer to [View problems and apply quick-fixes in the editor](linters.html#ws_js_linters_editor) and [Problems tool window](linters.html#ws_js_linters_general_problems_tool_window).

IntelliJ IDEA also provides code completion in JSCS configuration files.

### Before you start

  1. Download and install [Node.js](http://nodejs.org/#download). 

  2. Install and enable the JSCS plugin on the Settings | Plugins page, tab Marketplace, as described in [Installing plugins from JetBrains Marketplace](managing-plugins.html#install_plugin_from_repo). 

If the JSCS repository plugin is missing, IntelliJ IDEA suggests installing it when you open a .jscsrc or a .jscs.json configuration file.

![IntelliJ IDEA suggests installing JSCS plugin](https://resources.jetbrains.com/help/img/idea/2025.3/ws_jscs_install_plugin_from_config.png)



### Install JSCS globally

  * In the embedded Terminal (`Alt+F12`) , type:

`npm install --g jscs`




### Enable JSCS and configure its behavior in IntelliJ IDEA

  1. In the Settings dialog (`Ctrl+Alt+S`) , go to Languages & Frameworks | JavaScript | Code Quality Tools | JSCS. On the JSCS page, that opens, select the Enable checkbox. After that the other controls on the page become available.

  2. In the Node runtime field, specify the path to Node.js. If you followed the standard installation procedure, IntelliJ IDEA detects the path and fills in the field itself. 

  3. In the JSCS Package field, specify the location of the `jscs` package.

If you installed JSCS through the Node Package Manager, IntelliJ IDEA locates the package itself and fills in the field automatically. Otherwise, type the path manually or click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.openDiskHover.svg) and select the package location in the dialog that opens.

  4. Specify the configuration to use.

     * Search for config(s) \- select this option if JSCS rules are configured in your project package.json, in .jscsrc, or in .jscs .json.

IntelliJ IDEA will first look for a `jscsConfig` property in the project package .json.

If no `jscsConfig` property is found, IntelliJ IDEA will look for a .jscsrc or a .jscs.json configuration file. IntelliJ IDEA starts the search from the folder where the file to be checked is stored, then searches in the parent folder, and so on until the project root is reached.

     * Configuration File \- select this option if JSCS rules are configured in a custom JSON file. Specify the file location in the Path field. Select the path from the list or click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and select the relevant file in the dialog that opens.

  5. To apply a predefined set of rules associated with the code style you are using, select the set from the Code Style Preset list.

You can use the selected set independently or in addition to a configuration file. Note that rules from configuration files override predefined rules.




23 October 2025

[JSHint](jshint.html)[Closure Linter](closure-linter.html)
