[//]: # (Source: https://www.jetbrains.com/help/idea/typescript-compiler-tool-window.html)
[//]: # (Downloaded: 2025-12-17 20:04:54)

## Compile Errors

The tool window shows up only after you first compile your TypeScript code manually. This can be done in two ways:

  * Click the TypeScript widget on the Status bar, select Compile, and then select the compilation scope.

By default, Compile All stands for Compile all TypeScript files in the whole project. To change this behavior, define another scope under the `files` property of your tsconfig.json file. Type the names of the files to process in the following format: 

"files" : ["<file1.ts>","<file2.ts>"], 

![TypeScript: monitor compilation errors](https://resources.jetbrains.com/help/img/idea/2025.3/ws_ts_toolwindow_compilation_errors.png)
  * Select Compile TypeScript from the context menu of any TypeScript file. All the TypeScript files in the default scope will be compiled, as when you select Compile All from the TypeScript widget,




After that the tool window is accessible via View | Tool Windows | TypeScript in the main menu or via the tool window bar.

The tool window lists all the compilation errors detected in the chosen scope. This list is not affected by changes you make to your code and is updated only when you invoke compilation manually again.

Error messages are grouped by files in which they were detected. To navigate to the code in question, double-click the corresponding error message or select it and choose Jump to Source from the context menu. 
