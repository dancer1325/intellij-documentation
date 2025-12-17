[//]: # (Source: https://www.jetbrains.com/help/idea/node-debug-server-client.html)
[//]: # (Downloaded: 2025-12-17 19:33:08)

# Debugging the server- and the client-side code

Debugging of JavaScript client-side code is only supported in [Google Chrome](http://www.google.com/chrome/) and in other [Chromium-based browsers](https://www.chromium.org/). 

With IntelliJ IDEA, you can debug the server-side code of a Node.js application together with its client-side JavaScript code. To do that, you need to create and launch a JavaScript Debug configuration in addition to the Node.js configuration.

With IntelliJ IDEA, you can create a JavaScript Debug configuration from the Live Edit tab when creating or editing the main Node.js configuration. In this case, the JavaScript Debug configuration will start automatically every time you start the Node.js configuration.

![start debugging the server and the client code with one run/debug configuration](https://resources.jetbrains.com/help/img/idea/2025.3/node_debug_server_client.png)

Alternatively, create a JavaScript Debug configuration from the Edit Configurations dialog (Run | Edit Configurations) and then launch the configurations separately.

### Create two run/debug configurations

  1. From the list in the Run widget, select the Node.js run configuration to start together with a JavaScript Debug configuration. Then click ![the More button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moreVertical.svg) and select Edit from the menu.

![Select a Node.js run/debug configuration from the Run widget](https://resources.jetbrains.com/help/img/idea/2025.3/ws_node_run_config_select_edit.png)

Alternatively, create a new Node.js run configuration, as described in [Create a Node.js run/debug configuration](running-and-debugging-node-js.html#Node.js_run).

  2. The dialog that opens shows the settings of the selected Node.js run/debug configuration. Switch to the Browser / Live Edit tab.

![Run/Debug configurations: Node.js dialog, switch to the Browser/Live Edit tab](https://resources.jetbrains.com/help/img/idea/2025.3/ws_node_run_config_select_live_edit_tab.png)
  3. In the Browser / Live Edit tab, select After launch to start a browser automatically when you launch a debugging session. In the field below, type the URL address to open the application at.

Choose the browser to use from the list next to the After launch checkbox.

     * To use the system default browser, select Default.

     * To use a custom browser, select it from the list. Note that debugging of JavaScript client-side code is only supported in [Google Chrome](http://www.google.com/chrome/) and in other [Chromium-based browsers](https://www.chromium.org/).

     * To configure browsers, click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and adjust the settings in the Web Browsers and Preview dialog that opens. For more information, refer to [Web browsers](configuring-third-party-tools.html#web-browsers). 

Select the With JavaScript debugger checkbox.

![Node.js run/debug configuration: Browser/Live Edit tab](https://resources.jetbrains.com/help/img/idea/2025.3/ws_node_run_config_live_edit_tab.png)



### Start a session to debug the server and the client code

  1. From the list in the Run widget, select the modified Node.js run configuration and click ![the Debug icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.run.debug.svg) next to it.

![Start two run/debug configurations at once, select the main Node.js run/debug configuration](https://resources.jetbrains.com/help/img/idea/2025.3/node_debug_server_client_select_rc.png)
  2. The Debug tool window, that opens, has two tabs - a tab for the Node.js run/debug configuration and a tab for the Javascript Debug run/debug configuration. Which of the tabs is active depends on the location of the first hit breakpoint.

![Debug tool window with two tabs](https://resources.jetbrains.com/help/img/idea/2025.3/node_debug_server_client_debug_tool_window_two_tabs.png)

Proceed with the debugging session — [step through the breakpoints](stepping-through-the-program.html), switch between frames, change values on-the-fly, [examine a suspended program](examining-suspended-program.html), [evaluate expressions](examining-suspended-program.html#evaluating-expressions), and [set watches](examining-suspended-program.html#watches). 

  3. When the browser opens, perform the steps that will trigger the execution of the code. For example, navigate from the starting page of your application to another page in the browser. 

![Trigger app execution in the browser](https://resources.jetbrains.com/help/img/idea/2025.3/node_debug_server_client_browser_trigger_app.png)
  4. When the first breakpoint in the client-side code is hit, the application stops, the page in the browser is reloaded, and the focus in the Debug tool window moves to the tab with the JavaScript Debug configuration.

![The app is paused in the browser](https://resources.jetbrains.com/help/img/idea/2025.3/node_debug_server_client_paused_in_browser.png)

Continue with the debugging session — [step through the breakpoints](stepping-through-the-program.html), switch between frames, change values on-the-fly, [examine a suspended program](examining-suspended-program.html), [evaluate expressions](examining-suspended-program.html#evaluating-expressions), and [set watches](examining-suspended-program.html#watches). 




25 August 2025

[Running and debugging Node.js](running-and-debugging-node-js.html)[Multiprocess debugging](node-multiprocess-debugging.html)
