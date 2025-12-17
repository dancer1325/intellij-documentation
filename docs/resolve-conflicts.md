[//]: # (Source: https://www.jetbrains.com/help/idea/resolve-conflicts.html)
[//]: # (Downloaded: 2025-12-17 19:57:37)

## Productivity tips

Apply non-conflicting changes automatically
    

You can configure IntelliJ IDEA to always apply non-conflicting changes automatically instead of telling it to do so from the Merge dialog. To do this, select the Automatically apply non-conflicting changes option on the Tools | Diff Merge settings page `Ctrl+Alt+S`.

Manage changes in the central pane
    

You can manage changes in the central pane using the toolbar that appears when you hover over a change marker in the gutter and then click it. The toolbar is displayed together with a frame showing the previous contents of the modified line:

![the change toolbar](https://resources.jetbrains.com/help/img/idea/2025.3/conflicts_change_toolbar.png)

For example, when there are multiple non-conflicting changes, and you only need to skip one or two of them, it's easier to apply all of them simultaneously using the Apply all non-conflicting changes action and then undo the unwanted ones using the Revert action from this toolbar.
