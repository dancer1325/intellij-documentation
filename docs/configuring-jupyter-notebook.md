[//]: # (Source: https://www.jetbrains.com/help/idea/configuring-jupyter-notebook.html)
[//]: # (Downloaded: 2025-12-17 19:21:53)

## Kernel actions

### Restart kernel

You might want to refresh your calculations without shutting down the entire server and affecting any other notebooks. To restart the currently running kernel, click ![Kernels](https://resources.jetbrains.com/help/img/idea/2025.3/python-jupyter.icons.com.jetbrains.python.jupyter.expui.restartKernel.svg) on the [Jupyter notebook toolbar](jupyter-notebook-support.html#toolbar). You can then view the kernel status in the Server Log window:

![Restarting the current kernel](https://resources.jetbrains.com/help/img/idea/2025.3/py_jupyter_restart_kernel.png)




### Shutdown kernel

To completely stop a running kernel, open the list of servers on the Jupyter notebook toolbar and select Shutdown Kernel from the context menu. This action will terminate the current kernel session.

![Shutdown the kernel](https://resources.jetbrains.com/help/img/idea/2025.3/py_shutdown_kernel.png)




### Switch kernel

If you have at least two kernels available, and you need to switch to a different kernel, open the list of servers on the Jupyter notebook toolbar. Select Switch Kernel from the context menu and choose the required kernel from the dropdown list.

![Switch the kernel](https://resources.jetbrains.com/help/img/idea/2025.3/py_switch_kernel.png)




### Connect kernel to server

After selecting a remote Jupyter server and opening a notebook, the kernel list becomes available automatically after the first cell is run.

However, you can manually connect to the server before running any cells. After adding the external server, click the ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.refresh.svg) Connect to Server button on the [Jupyter notebook toolbar](jupyter-notebook-support.html#toolbar). This will establish the connection between the kernel and the Jupyter server.

![Connect the kernel to the server](https://resources.jetbrains.com/help/img/idea/2025.3/py_connect_kernel.png)



