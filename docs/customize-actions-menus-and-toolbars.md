[//]: # (Source: https://www.jetbrains.com/help/idea/customize-actions-menus-and-toolbars.html)
[//]: # (Downloaded: 2025-12-17 19:23:43)

## Customize the main toolbar

### Quickly add actions to the toolbar

If you miss an action on the main toolbar, you can add it from the list of popular actions.

  * Right-click the toolbar, point to Add Action to Main Toolbar, and select the action that you want to add from the list.

If the action that you want to add is not on the list of popular actions, use the [Customize Main Toolbar](#configure-toolbar-actions) dialog.

![Adding actions to main toolbar](https://resources.jetbrains.com/help/img/idea/2025.3/quickly_add_toolbar_actions.png)



The selected action appears on the toolbar. You can remove it or change its icon using the [Customize Main Toolbar](#configure-toolbar-actions) dialog.

### Configure main toolbar actions

Use this option to access all available actions that can be added to the main toolbar. It also allows you to change icons for toolbar actions and remove actions from the toolbar.

  1. Right-click the toolbar and click Customize Toolbar.

  2. In the list of available toolbar sections, expand the node you want to customize and select the desired item:

     * Click Add to add an action or a separator under the selected item.

     * Click ![the Remove button](https://resources.jetbrains.com/help/img/idea/2025.3/app.resharper.expui.Common.Remove.png) to remove the selected item.

     * Click ![the Edit Icon button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.edit.svg) to [add or change the icon](#custom-icons-menu) for the selected action.

     * Click ![the Move Up button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.moveUp.svg) or ![the Move Down button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.moveDown.svg) to move the selected item up or down. By doing so, you can change the action's location in the menu.

     * Click ![the Restore button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.vcs.revert.svg) to restore the selected action or all actions to default settings.

  3. Click OK to save your changes.




### Configure the toolbar color

Use colored headers to simplify navigation between several open projects. You can assign a unique color and [icon](#change-project-icon) to each of your projects, making it easier to distinguish them in your workspace.

By default, the IDE picks the color that matches the color of the project [icon](#change-project-icon), but you can set your own color.

  1. Right-click the toolbar, select Change Project Color, and choose one of the pre-defined colors from the list.

![Configuring the main toolbar color](https://resources.jetbrains.com/help/img/idea/2025.3/change_main_toolbar_color.png)
  2. If you want to use a different color, click Custom Color and select a shade using the color picker that opens.




To turn the feature off, right-click the toolbar and disable the Show Project Gradient option. You can also disable colors in settings: press `Ctrl+Alt+S`, select Appearance & Behavior | Appearance and disable Use project colors in main toolbar.

### Change the project icon

  1. Right-click the toolbar and click Set Custom Project Icon.

  2. In the dialog that opens, click Choose SVG file and specify the path to the SVG file that you want to use as an icon.

  3. Click OK to save your changes.




### Hide the toolbar

If you prefer to have less visual clutter in your IDE window, you can hide the toolbar.

  * In the main menu, go to View | Appearance and disable Toolbar.

When the toolbar is hidden, the IDE window header has a plain look without any IntelliJ IDEA widgets or controls.

![IDE window with the toolbar hidden](https://resources.jetbrains.com/help/img/idea/2025.3/ide_without_toolbar.png)


