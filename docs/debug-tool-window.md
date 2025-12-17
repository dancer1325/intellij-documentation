[//]: # (Source: https://www.jetbrains.com/help/idea/debug-tool-window.html)
[//]: # (Downloaded: 2025-12-17 19:24:18)

## Sessions

The available debug sessions are separated into tabs in the top part of the Debug tool window.

![Session tabs](https://resources.jetbrains.com/help/img/idea/2025.3/debug_session_tabs.png)

If you [enable the Services tool window](using-services-tool-window.html) for specific run/debug configurations, the entire view of the Debug tool window will be displayed inside the Services tool window when you debug any of these configurations.

All the information in the editor, like [inline variable values](examining-suspended-program.html#inline-view) and execution point, is shown for the selected session tab. This is important if you are running several debug sessions in parallel that use the same classes.

![Inline variables view and execution point for the current session](https://resources.jetbrains.com/help/img/idea/2025.3/debug_session_tabs_example.png)

When you close a tab, the corresponding debug session terminates.
