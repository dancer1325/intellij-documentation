[//]: # (Source: https://www.jetbrains.com/help/idea/node-interactive-debugger-console.html)
[//]: # (Downloaded: 2025-12-17 19:33:09)

# Using interactive Debugger Console

When you are debugging a Node.js application, IntelliJ IDEA shows two console tabs in the Debug tool window - Process Console and Debugger Console.

  * The Process Consoletab shows the output of the node process itself, that is, everything that is written to [process.stdout](https://nodejs.org/api/process.html#process_process_stdout) and [process.stderr](https://nodejs.org/api/process.html#process_process_stderr) directly or is logged using [console.*](https://nodejs.org/api/console.html#console_class_console). 

![Node.js debugging session: Process Console](https://resources.jetbrains.com/help/img/idea/2025.3/ws_node_debugging_process_console.png)
  * In the Debugger Console, you can run JavaScript code snippets and view the [console.*](https://nodejs.org/api/console.html#console_console) messages.




### Run JavaScript in the Debugger Console

  1. Start typing a statement at `>` in the input field. As you type, IntelliJ IDEA suggests variants for completion. 

When typing a multi-line code fragment, press `Shift+Enter` to start a new line and `Ctrl+Enter` to split a line.

  2. Select the relevant statement and press `Enter`. IntelliJ IDEA shows its value in the debugger console. 

IntelliJ IDEA shows previews for objects, so you do not need to expand them. If you still expand an object, you get an overview of just its own properties, the `__proto__` contents are hidden by default.




### Navigate to source code

  * At each line with output of `console.*`, IntelliJ IDEA shows the name of the file and the line where it was called. Click this link to jump to the call in the source code. 

![Node.js interactive debugger console: navigation to source code](https://resources.jetbrains.com/help/img/idea/2025.3/node_interactive_debugger_console_navigate_to_source.png)
  * The Debugger Console also shows stack traces. Click the link next to a reported problem to jump to the line of code where this problem occurred. 

![Node.js interactive debugger console: navigation to errors](https://resources.jetbrains.com/help/img/idea/2025.3/node_interactive_debugger_console_navigate_from_stack_trace.png)



### Filter out messages

The Debugger Console tab shows objects in a tree view, with stack traces collapsed by default. Warnings `console.warn()`, errors `console.error()`, and info `console.info()` messages have different icons and background colors to make them easier to notice. 

  * To hide log messages of specific types, click ![the Filter button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.filter.svg) and select the severities to filter out.

![Node.js interactive debugger console: filtering out messages by type](https://resources.jetbrains.com/help/img/idea/2025.3/node_interactive_debugger_console_filter.png)



### Group messages

  * The log messages grouped using `console.group()` and `console.groupEnd()` are displayed as a tree. To show the output collapsed by default, use `console.groupCollapsed()`. 

![Node.js interactive debugger console: log messages grouped](https://resources.jetbrains.com/help/img/idea/2025.3/node_interactive_debugger_console_group_messages.png)



### Apply CSS styles

  * Use CSS and the `%c` marker to apply styles to log messages.

![Node.js interactive debugger console: applying CSS style to log messages](https://resources.jetbrains.com/help/img/idea/2025.3/node_interactive_debugger_console_css.png)

For more information, refer to [Styling console output with CSS](https://developers.google.com/web/tools/chrome-devtools/console/console-write#styling_console_output_with_css). 




25 August 2025

[Multiprocess debugging](node-multiprocess-debugging.html)[Live Edit in Node.js applications](live-editing-in-node-js-applications.html)
