[//]: # (Source: https://www.jetbrains.com/help/idea/node-multiprocess-debugging.html)
[//]: # (Downloaded: 2025-12-17 19:33:12)

# Multiprocess debugging

With IntelliJ IDEA, you can debug additional Node.js processes that are launched by the [child_process.fork() method](https://nodejs.org/api/child_process.html#child_process_child_process_fork_modulepath_args_options) or by the [cluster module](https://nodejs.org/api/cluster.html). Such processes are shown as threads in the Frames pane on the Debugger tab of the [Debug tool window](debug-tool-window.html).

![Node.js application: Multi-process debugging](https://resources.jetbrains.com/help/img/idea/2025.3/ws_node_multiprocess.png)

  1. Set the [breakpoints](using-breakpoints.html) in the processes to debug.

  2. Create a Node.js run/debug configuration as described in [Running and Debugging Node.js](running-and-debugging-node-js.html#Node.js_run). 

  3. From the Run widget list on the toolbar, select the newly created  configuration and click ![the Debug button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.run.debug.svg) next to it. 

The [Debug tool window](debug-tool-window.html) opens and the Frames list shows the additional processes as threads as soon as they are launched.

To examine the data (variables, watches, and so on) for a process, select its thread in the list and view its data in the Variables and Watches panes. When you select another process, the contents of the panes are updated accordingly.




25 August 2025

[Debugging the server- and the client-side code](node-debug-server-client.html)[Using interactive Debugger Console](node-interactive-debugger-console.html)
