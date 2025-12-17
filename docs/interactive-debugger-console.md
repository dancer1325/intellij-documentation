[//]: # (Source: https://www.jetbrains.com/help/idea/interactive-debugger-console.html)
[//]: # (Downloaded: 2025-12-17 19:29:56)

# Interactive debugger console

  * The interactive Console pane is shown only when you are [debugging an application](debugging-javascript-in-chrome.html) or [debugging a test](unit-testing-javascript.html#running-and-debugging-tests). It is not available when you are [running an application](running-applications.html) or [previewing web pages](editing-html-files.html#ws_html_preview_output).

  * Debugging of JavaScript code is only supported in [Google Chrome](http://www.google.com/chrome/) and in other [Chromium-based browsers](https://www.chromium.org/). 




The interactive Console pane shows you stack traces and everything that was logged in your code (for example, using `console.*`).

The Console pane is also a read-eval-print loop (REPL) so you can run JavaScript code snippets in it and interact with the page that you are currently debugging.

### Run JavaScript in the Console

  1. Start typing a statement at `>` in the input field. As you type, IntelliJ IDEA suggests variants for completion. 

  2. Select the relevant statement and press `Enter`. IntelliJ IDEA shows its value in the console. 

IntelliJ IDEA shows previews for objects, so you do not need to expand them. If you still expand an object, you get an overview of just its own properties, the `__proto__` contents are hidden by default.




### Navigate to source code

  * At each line with output of `console.*`, IntelliJ IDEA shows the name of the file and the line where it was called. Click this link to jump to the call in the source code. 

![JavaScript interactive debugger console: navigation to source code](https://resources.jetbrains.com/help/img/idea/2025.3/js_interactive_debugger_console_navigate_to_source.png)
  * The Console also shows stack traces. Click the link next to a reported problem to jump to the line of code where this problem occurred. 

![JavaScript interactive debugger console: navigation to errors](https://resources.jetbrains.com/help/img/idea/2025.3/js_interactive_debugger_console_navigate_from_stack_trace.png)



### Filter out messages

The Console tab shows objects in a tree view, with stack traces collapsed by default. Warnings `console.warn()`, errors `console.error()`, and info `console.info()` messages have different icons and background colors to make them easier to notice. 

  * To hide log messages of specific types, click ![the Filter button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.filter.svg) and select the severities to filter out.

![Node.js interactive debugger console: filtering out messages by type](https://resources.jetbrains.com/help/img/idea/2025.3/js_interactive_debugger_console_filter.png)



### Group messages

  * The log messages grouped using `console.group()` and `console.groupEnd()` are displayed as a tree. To show the output collapsed by default, use `console.groupCollapsed()`. 

![Node.js interactive debugger console: log messages grouped](https://resources.jetbrains.com/help/img/idea/2025.3/js_interactive_debugger_console_group_messages.png)



### Apply CSS styles

  * Use CSS and the `%c` marker to apply styles to log messages.

![JavaScript interactive debugger console: applying CSS style to log messages](https://resources.jetbrains.com/help/img/idea/2025.3/js_interactive_console_css.png)

For more information, refer to [Styling console output with CSS](https://developers.google.com/web/tools/chrome-devtools/console/console-write#styling_console_output_with_css). 




05 August 2025

[Debug JavaScript in Chrome](debugging-javascript-in-chrome.html)[Configuring JavaScript debugger](configuring-javascript-debugger.html)
