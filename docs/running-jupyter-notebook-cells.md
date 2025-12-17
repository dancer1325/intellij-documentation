[//]: # (Source: https://www.jetbrains.com/help/idea/running-jupyter-notebook-cells.html)
[//]: # (Downloaded: 2025-12-17 19:59:26)

## Run code cells

### Run code cells using shortcuts and toolbar options

  * Use the following smart shortcuts to quickly run the code cells:

    * `Ctrl+Enter`: Runs the current cell.

    * `Shift+Enter`: Runs the current cell and selects the cell below it.

When executing one cell at a time, mind code dependencies. If a cell relies on some code in another cell, that cell should be executed first.

When the execution is done, the cell remains in the edit mode so that you can modify it, if needed, and keep experimenting.

Press `Ctrl+Home` to move the caret to the start or `Ctrl+End` to move the caret to the end of the current cell while in edit mode.

  * To execute all code cells in your notebook, click ![Run all](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.actions.runAll.svg) on the [notebook toolbar](jupyter-notebook-support.html#toolbar).

  * Press `Ctrl+Home` to focus on the fist cell or `Ctrl+End` to focus on the last cell of your notebook while in command mode.




### Duration of cell execution

  * You can find the information about the duration of a cell execution in the lower left corner of the cell.

Hover over this area to view the date and time when the cell execution was completed.

![The information about the last cell execution](https://resources.jetbrains.com/help/img/idea/2025.3/last_cell_execution_info.png)

In case of any errors, expand the Traceback node to view the complete error message.

![Error traceback](https://resources.jetbrains.com/help/img/idea/2025.3/py_ds_error_traceback.png)



When you [stop the server](configuring-jupyter-notebook.html#stop-server) and [change the server or kernel](configuring-jupyter-notebook.html#setup-configured-server), you have to execute all cells with dependencies again because execution results are valid for the current server session only.
