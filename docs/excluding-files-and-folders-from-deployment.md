[//]: # (Source: https://www.jetbrains.com/help/idea/excluding-files-and-folders-from-deployment.html)
[//]: # (Downloaded: 2025-12-17 19:25:59)

## Exclude a folder on server from upload/download after project creation

### Add a folder to the list of excluded paths

  1. Open the [Deployment](settings-deployment.html) dialog by doing one of the following:

     * Choose Tools | Deployment | Configuration from the main menu.

     * In the Settings dialog (`Ctrl+Alt+S`) , select Deployment under Build, Execution, Deployment.

  2. In the [Deployment](settings-deployment.html)

dialog, click the [Excluded Paths](deployment-excluded-paths-tab.html) tab. The tab shows the list of the previously excluded local and remote folders.

  3. Click the Add button ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select Deployment path.

  4. Double-click the empty line that is added to the list.

  5. At the end of the added line, click the Browse button ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.open.svg).

  6. In the Choose remote excluded path dialog, navigate to the folder that you want to exclude.

You can also type the path manually, but note that only absolute paths are accepted.

  7. When you click OK, you return to the [Excluded Paths](deployment-excluded-paths-tab.html) tab, where the selected remote folder is added to the list.




### Add a folder to the list of excluded paths in the Remote Host tool window

  1. In the main menu, go to Tools | Deployment | Browse Remote Host or View | Tool Windows | Remote Host.

  2. In the [Remote Host](remote-host-tool-window.html) tool window that opens, select the relevant [server configuration](creating-in-place-server-configuration.html) from the list.

  3. Select the folder to exclude and choose Exclude Path from the context menu of the selection.



