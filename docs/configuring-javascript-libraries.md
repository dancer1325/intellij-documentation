[//]: # (Source: https://www.jetbrains.com/help/idea/configuring-javascript-libraries.html)
[//]: # (Downloaded: 2025-12-17 19:21:51)

## Download TypeScript community stubs (TypeScript definition files)

TypeScript community stubs are also known as TypeScript definition files, or TypeScript declaration files, or DefinitelyTyped stubs, or just d.ts files.

In IntelliJ IDEA, [DefinitelyTyped stubs](https://github.com/DefinitelyTyped/DefinitelyTyped) can be configured and used as libraries, which is in particular helpful in the following cases:

  * To improve code completion, resolve symbols for a library or a framework that is too sophisticated for IntelliJ IDEA static analysis, and add type information for such symbols.

  * To resolve globally defined symbols from test frameworks.




The example below shows a piece of code from an Express application where the `post()` function is not resolved:

![Symbol not resolved without d.ts](https://resources.jetbrains.com/help/img/idea/2025.3/ws_js_configure_libraries_node_express_symbols_not_resolved_without_d_ts.png)

IntelliJ IDEA successfully resolves `post()` after you install a TypeScript definition file:

![Symbol resolved after d.ts is installed](https://resources.jetbrains.com/help/img/idea/2025.3/ws_js_configure_libraries_node_express_symbols_resolved_with_d_ts.png)

With IntelliJ IDEA lets you download TypeScript definition files right from the editor, using an intention action, or you can do it on the Settings: JavaScript Libraries page.

### Download TypeScript definitions using an intention action

  * Place the caret at the `import` or `require` statement with this library or framework, press `Alt+Enter`, and choose Install TypeScript definitions for better type information:

![Download TypeScript definitions intention action](https://resources.jetbrains.com/help/img/idea/2025.3/ws_js_libs_download_ts_definitions_intention_action.png)

IntelliJ IDEA downloads the type definitions for the library and adds them to the list of libraries on the JavaScript. Libraries page:

![Type definitions library added to the list](https://resources.jetbrains.com/help/img/idea/2025.3/ws_js_libs_download_ts_definitions_added_to_lib_list.png)
  * Alternatively, open your package.json, place the caret at the package to download a type definition for, press `Alt+Enter`, and select Install '@types/<package name>'.

![Install type definitions from package.json](https://resources.jetbrains.com/help/img/idea/2025.3/ws_js_libs_download_ts_definitions_from_package_json.png)



### Download TypeScript definitions on the JavaScript Libraries page

  1. Press `Ctrl+Alt+S` to open settings and then select Languages & Frameworks | JavaScript | Libraries.

  2. On the Libraries page that opens, click Download and in the Download Library dialog that opens, select the required library, and click Download and Install.

![Add TypeScript definition file](https://resources.jetbrains.com/help/img/idea/2025.3/ws_js_configure_libraries_download_ts_community_stubs.png)



IntelliJ IDEA shows the downloaded type definitions in the Project tool window `Alt+1`, under the External Libraries node.

![Downloaded type definitions are shown under the External libraries node](https://resources.jetbrains.com/help/img/idea/2025.3/ws_js_libs_download_ts_definitions_shown_in_external_libraries.png)

### Optionally

  * IntelliJ IDEA enables the downloaded type definitions in the scope of the current project. You can change this scope as described in [Configuring the scope of a library](#ws_js_configuring_js_libs_change_scope) below. See also [Example: Configuring the scope for HTML and Node.js Core libraries](#ws_js_external_libraries_configuring_html_and_node_core).



