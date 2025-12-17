[//]: # (Source: https://www.jetbrains.com/help/idea/jslint.html)
[//]: # (Downloaded: 2025-12-17 19:30:45)

# JSLint

Since IntelliJ IDEA 2020.2, [JSLint](https://www.jslint.com) support in the IDE has been deprecated.

However, JSLint support is still available through the JSLint plugin, which can be installed on the Settings | Plugins page as described in [Installing plugins from JetBrains Marketplace](managing-plugins.html#install_plugin_from_repo). 

Note that JSLint does not fully support some latest ECMAScript features. For more information, refer to [JSLint official website](https://jslint.com/help.html#es6).

When [JSLint support is enabled](#ws_js_linters_jslint_enable_and_configure), IntelliJ IDEA highlights errors that JSLint detects, provides descriptions for them, and suggests quick-fixes where possible.

Descriptions of the errors detected in the current file and quick-fixes for them are available from the editor and from the File tab of the [Problems](linters.html#ws_js_linters_general_problems_tool_window) tool window.

Errors in all previously opened files and quick-fixes for them are shown in the Project Errors tab of the Problems tool window. To open the tool window, click the Inspection widget in the upper-right corner of the editor:

![Inspection widget](https://resources.jetbrains.com/help/img/idea/2025.3/inspection-widget.png)

For more information, refer to [View problems and apply quick-fixes in the editor](linters.html#ws_js_linters_editor) and [Problems tool window](linters.html#ws_js_linters_general_problems_tool_window).

### Before you start

  * Install and enable the JSLint plugin on the Settings | Plugins page, tab Marketplace, as described in [Installing plugins from JetBrains Marketplace](managing-plugins.html#install_plugin_from_repo). 




### Enable JSLint and configure its behavior in IntelliJ IDEA

  1. In the Settings dialog (`Ctrl+Alt+S`) , go to Languages & Frameworks | JavaScript | Code Quality Tools | JSLint, and select the Enable checkbox. After that the other controls on the page become available.

  2. By default, the tool reports detected problems of all types. To skip problems of a certain type, select the checkbox next to this type in the Tolerate area.

Learn more about JSLint options from the [JSLint official website](https://www.jslint.com/help.html#browser).

  3. In the Assume area, specify the targeted environment to check the code against.

  4. In the Globals field, specify the predefined [global variables](https://jslint.com/help.html#global). Type their names or use `predef` object keys.

  5. To verify .json files as well, select the JSON checkbox In the Validate also area.




08 August 2025

[ESLint](eslint.html)[JSHint](jshint.html)
