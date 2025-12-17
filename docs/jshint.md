[//]: # (Source: https://www.jetbrains.com/help/idea/jshint.html)
[//]: # (Downloaded: 2025-12-17 19:30:44)

# JSHint

You can check your code with the [JSHint](http://jshint.com/about/) linter which is already bundled with IntelliJ IDEA.

When [JSHint support is enabled](#ws_js_linter_jshint_enable), IntelliJ IDEA highlights errors that JSHint detects, provides descriptions for them, and suggests quick-fixes where possible.

Descriptions of the errors detected in the current file and quick-fixes for them are available from the editor and from the File tab of the [Problems](linters.html#ws_js_linters_general_problems_tool_window) tool window.

Errors in all previously opened files and quick-fixes for them are shown in the Project Errors tab of the Problems tool window. To open the tool window, click the Inspection widget in the upper-right corner of the editor:

![Inspection widget](https://resources.jetbrains.com/help/img/idea/2025.3/inspection-widget.png)

For more information, refer to [View problems and apply quick-fixes in the editor](linters.html#ws_js_linters_editor) and [Problems tool window](linters.html#ws_js_linters_general_problems_tool_window).

### Enable JSHint and configure its behavior in IntelliJ IDEA

  1. In the Settings dialog (`Ctrl+Alt+S`) , go to Languages & Frameworks | JavaScript | Code Quality Tools | JSHint.

  2. On the JSHint page that opens, select the Enable checkbox. After that all the controls on the page become available.

  3. In the Version field, specify the version of the tool to use. IntelliJ IDEA comes bundled with version 2.10.2, which is used by default. To download another version, select it from the list.

  4. Configure JSHint behavior in IntelliJ IDEA

     * Use config files \- select this checkbox to apply JSHint rules from a custom configuration file, or from a  .jshintrc file, or from a package.json, under the `jshintConfig` property.

Select the Default option if the rules are configured in a  .jshintrc file or under the `jshintConfig` property in a package.json. IntelliJ IDEA will first look for such configuration in the folder where the file to be checked is stored, then in its parent folder, and so on until the filesystem root is reached.

Alternatively, select Custom configuration file and specify the file location in the Path field below.

Learn more about JSHint configuration files from the [JSHint official website](http://jshint.com/docs/).

     * To configure verification rules manually, clear the Use config files checkbox and enable the relevant validations in the Options area. Learn more from the [JSHint official website](http://jshint.com/docs/options/).




08 October 2024

[JSLint](jslint.html)[JSCS](jscs.html)
