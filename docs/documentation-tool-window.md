[//]: # (Source: https://www.jetbrains.com/help/idea/documentation-tool-window.html)
[//]: # (Downloaded: 2025-12-17 19:25:20)

# Documentation tool window

By default, IntelliJ IDEA shows [Quick Documentation](viewing-reference-information.html#inline-quick-documentation) in a popup; to view it in the tool window, click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.more.svg) in the popup and choose Open in Documentation Tool Window or press `Ctrl+Q` twice.

The feature allows you to access both downloaded documentation and external documentation for which you only specify its URL. For more information about adding code documentation, refer to:

  * [Configure library documentation](library.html#add-library-docs)

  * [Configure SDK documentation](configure-sdk-documentation.html)


![IntelliJ IDEA: Documentation tool window](https://resources.jetbrains.com/help/img/idea/2025.3/quick-doc-toolwindow.png)

The View | Tool Windows | Documentation menu option appears only if you have configured the IDE to display [code documentation](viewing-reference-information.html#inline-quick-documentation) in a tool window and some documentation is open in the window.

Icon| Shortcut| Description  
---|---|---  
![the Back button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.left.svg) ![the Forward button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.right.svg)| `Left` or `Right`| Switch to the previous or go to the next documentation page (for example, after clicking hyperlinks).On macOS, you can also use the three-finger right-to-left and left-to-right swipe gestures.  
![the Edit Source button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.edit.svg)| `F4`| Navigate to the source code of the symbol whose documentation is currently open.  
![Settings](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moreVertical.svg)| | 

  * Show Documentation Popup First: show documentation in a popup when you press `Ctrl+Q`. Press `Ctrl+Q` the second time to open the documentation in the tool window.Disable the option to always show quick documentation in the tool window.
  * Show on Mouse Move: show quick documentation when you hover over code elements in the editor. When the option is disabled, you need to press `Ctrl+Q` to view code documentation.
  * Open as Popup `Ctrl+Q`: show code documentation in a popup instead of the tool window.
  * Auto-update from Source: when this option is enabled, the content of the tool window changes as you move the mouse pointer in the editor.If the [Show on Mouse Move](viewing-reference-information.html#disable-auto-quick-documentation) option is disabled, place the caret at the symbol and press `Ctrl+Q` to see its documentation in the tool window.
  * Close All: close the tool window and all currently open tabs.
  * Adjust Font Size: display a slider for changing the font size.
  * View Mode: by default, the tool window is attached to the edge of the main window and is always visible. You can change the [view mode](viewing-modes.html), for example, to make it visible only when active or to detach it from the tool window bar.
  * Move to: select where to attach the tool window.
  * Resize: adjust the size of the tool window.
  * Remove from Sidebar: close the tool window. To reopen it, select View | Tool Windows | Documentation from the main menu.

  
  
06 May 2024

[CDI tool window](cdi-tool-window.html)[Duplicates tool window](duplicates-tool-window.html)
