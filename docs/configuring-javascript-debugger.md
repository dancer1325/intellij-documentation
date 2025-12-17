[//]: # (Source: https://www.jetbrains.com/help/idea/configuring-javascript-debugger.html)
[//]: # (Downloaded: 2025-12-17 19:21:50)

## Customize the default debugger configuration

### Suppress calls

  1. Open settings by pressing `Ctrl+Alt+S` and navigate to Build, Execution, Deployment | Debugger. 

  2. Suppress calls to the files on the built-in server from other computers or from outside IntelliJ IDEA by clearing the Can accept external connections or the Allow unsigned requests checkbox respectively.

![Suppress external calls](https://resources.jetbrains.com/help/img/idea/2025.3/ij_js_debugger_suppress_external_calls.png)



### Choose the way to remove breakpoints

By default, you can toggle breakpoints by clicking the left mouse button. To change this behavior:

  1. Open settings by pressing `Ctrl+Alt+S` and navigate to Build, Execution, Deployment | Debugger. 

  2. In the Remove breakpoint area, select the appropriate option.

![Remove breakpoints](https://resources.jetbrains.com/help/img/idea/2025.3/ij_js_debugger_remove_breakpoints.png)



### Advanced options

  * Open settings by pressing `Ctrl+Alt+S` and navigate to Build, Execution, Deployment | Debugger | Data Views. 

Enable or disable [Inline Debugging](examining-suspended-program.html#inline-view), specify when you want to see tooltips with object values and [expressions evaluation results](examining-suspended-program.html#evaluating-expressions), and so on.

![JavaScript debugger: Data views](https://resources.jetbrains.com/help/img/idea/2025.3/js_debugger_data_views.png)
  * Open settings by pressing `Ctrl+Alt+S` and navigate to Build, Execution, Deployment | Debugger | Data Views | JavaScript. 

Specify whether you want object properties to be shown in object nodes. If so, specify the properties. Use ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg) to manage the list of properties.

![Properties to show on object nodes](https://resources.jetbrains.com/help/img/idea/2025.3/js_debugger_object_node.png)


