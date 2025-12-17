[//]: # (Source: https://www.jetbrains.com/help/idea/closure-linter.html)
[//]: # (Downloaded: 2025-12-17 19:20:04)

# Closure Linter

Since IntelliJ IDEA 2020.2, Closure Linter support in the IDE has been deprecated. For more information, refer to the [Closure Linter official website](https://developers.google.com/closure/utilities/).

However, Closure Linter support is still available through the Closure Linter plugin, which can be installed on the Settings | Plugins page as described in [Installing plugins from JetBrains Marketplace](managing-plugins.html#install_plugin_from_repo). 

When [Closure Linter support is enabled](#ws_js_linters_closure_linter_enable), IntelliJ IDEA highlights errors that Closure Linter detects, provides descriptions for them, and suggests quick-fixes where possible.

Descriptions of the errors detected in the current file and quick-fixes for them are available from the editor and from the File tab of the [Problems](linters.html#ws_js_linters_general_problems_tool_window) tool window.

Errors in all previously opened files and quick-fixes for them are shown in the Project Errors tab of the Problems tool window. To open the tool window, click the Inspection widget in the upper-right corner of the editor:

![Inspection widget](https://resources.jetbrains.com/help/img/idea/2025.3/inspection-widget.png)

For more information, refer to [View problems and apply quick-fixes in the editor](linters.html#ws_js_linters_editor) and [Problems tool window](linters.html#ws_js_linters_general_problems_tool_window).

### Before you start

  1. Download and install Python as described on the [Python official website](https://www.python.org/downloads/).

  2. Install and enable the Closure Linter plugin on the Settings | Plugins page, tab Marketplace, as described in [Installing plugins from JetBrains Marketplace](managing-plugins.html#install_plugin_from_repo). 

  3. Download and install Closure Linter as described on the [Closure official website](https://developers.google.com/closure/utilities/docs/linter_howto#install-closure-linter).




### Enable Closure Linter and configure its behavior in IntelliJ IDEA

  1. Open the Settings dialog (`Ctrl+Alt+S`) , go to Languages & Frameworks | JavaScript | Code Quality Tools | Closure Linter, select the Enable checkbox. After that all the controls on the page become available.

  2. Specify the path to the Closure Linter executable file:

     * <Python_home>\Scripts\gjslint.exe for Windows

     * /usr/local/bin/gjslint for Linux and macOS

  3. Specify the path to the previously created configuration file with [Closure Linter flags](https://developers.google.com/closure/utilities/docs/linter_howto#find-style-problems).




08 August 2025

[JSCS](jscs.html)[Minifying JavaScript](minifying-javascript.html)
