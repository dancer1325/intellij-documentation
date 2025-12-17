[//]: # (Source: https://www.jetbrains.com/help/idea/settings-languages-javascript.html)
[//]: # (Downloaded: 2025-12-17 20:01:15)

# JavaScript

The page is available only when the JavaScript and Typescript plugin is enabled on the Settings | Plugins page as described in [Managing plugins](managing-plugins.html). 

Item| Description  
---|---  
JavaScript Language Version| From this list, select the JavaScript language version that represents the set of the language features to use in your project. The available options are:

  * [ECMAScript 5.1](http://www.ecma-international.org/ecma-262/5.1/)
  * [ECMAScript 6+](http://www.ecma-international.org/ecma-262/6.0/): This version adds support for the features introduced in ECMAScript 2015-2020 and for JSX syntax as well as some current proposals to the standard.
  * [Flow](https://flow.org/): This version adds support for the Flow syntax.

To use multiple JavaScript versions in your project, click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.moreHorizontal.svg) and specify JavaScript versions for specific folders, learn more from [Use multiple JavaScript versions](javascript-specific-guidelines.html#ws_js_choose_language_version_multiple_versions).![Choose language versions for separate folders](https://resources.jetbrains.com/help/img/idea/2025.3/ws_js_choose_language_version.png)  
Configure code completion settings| Click this link to open the [Code Completion page](auto-completing-code.html#code_completion_options) and configure completion in the JavaScript context.  
Flow package or executable| In this field, specify the path to the node_modules\flow-bin package or the Flow binary executable file. To use node_modules\\.bin\flow, make sure the path to Node.js is added to the `PATH` environment variable.  The field is available only when Flow is chosen from the JavaScript Language Version list.   
Use Flow server for:| In this area, specify the basis for coding assistance by selecting or clearing the following checkboxes: 

  * Type checking: When this checkbox is selected, syntax and error highlighting is provided based on the data received from the Flow server. When the checkbox is cleared, only the basic internal IntelliJ IDEA highlighting is available. 
  * Navigation, code completion, and type hinting: When this checkbox is selected, suggestion lists for reference resolution and code completiong contain both suggestions retrieved from integration with Flow and suggestions calculated by IntelliJ IDEA. When the checkbox is cleared, references are resolved through IntelliJ IDEA calculation only. 

The checkboxes are available only when the path to the Flow executable file is specified.   
Save all modified files automatically| Keep this checkbox selected to ensure that Flow is applied continuously because Flow checks the current files only after all the other modified files are saved.  
  
25 July 2025

[Languages and Frameworks](settings-languages-and-frameworks.html)[JavaScript Runtime](javascript-runtime.html)
