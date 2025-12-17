[//]: # (Source: https://www.jetbrains.com/help/idea/live-editing-in-node-js-applications.html)
[//]: # (Downloaded: 2025-12-17 19:31:31)

# Live Edit in Node.js applications

Live Edit is available only during a [Node.js debugging session](running-and-debugging-node-js.html#node_debugging_overview) in [Google Chrome](http://www.google.com/chrome/) and in other [Chromium-based browsers](https://www.chromium.org/).

Learn more from [Live Edit in HTML, CSS, and JavaScript](live-editing.html).

With the Live Edit functionality, the changes you make to your HTML, CSS, or JavaScript code are immediately shown in the browser without reloading the page.

Live Edit works for other file types that contain or generate HTML, CSS, or JavaScript.

By default, Live Edit is enabled only in HTML and CSS files.

### Before you start

  1. Make sure you have [Node.js](http://nodejs.org/) on your computer. 

  2. Make sure the JavaScript and TypeScript, JavaScript Debugger, and Node.js required plugins are enabled on the Settings | Plugins page, tab Installed. For more information, refer to [Managing plugins](managing-plugins.html). 

  3. Install and enable the Live Edit plugin on the Settings | Plugins page, tab Marketplace, as described in [Installing plugins from JetBrains Marketplace](managing-plugins.html#install_plugin_from_repo). 




### Enable Live Edit

  1. Press `Ctrl+Alt+S` to open settings and then select Build, Execution, Deployment | Debugger | Live Edit.

  2. Select Update Node.js application on changes. Specify the time-delay between changing the code in the editor and showing this change in the browser: accept the default value `300 ms` or specify a custom value using the spin box next to the corresponding field. 




25 August 2025

[Using interactive Debugger Console](node-interactive-debugger-console.html)[Testing Node.js](unit-testing-node-js.html)
