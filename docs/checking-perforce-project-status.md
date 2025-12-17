[//]: # (Source: https://www.jetbrains.com/help/idea/checking-perforce-project-status.html)
[//]: # (Downloaded: 2025-12-17 19:19:53)

# Check Perforce project status

Besides indicating the [current file status](adding-files-to-version-control.html#file_status) relative to the repository, IntelliJ IDEA integration with Perforce provides you with the accumulated view of the project files' statuses.

### View differences between the current state of the project files and the repository

  1. Open the required project.

  2. In the main menu, go to VCS | Refresh File Status.

  3. Open the Commit tool window `Alt+0`. 

  4. The status of each file is indicated by the [color](adding-files-to-version-control.html#file_status) in which the path to the file is displayed. 

![checkProjectStatusPerforce.png](https://resources.jetbrains.com/help/img/idea/2025.3/checkProjectStatusPerforce.png)



### Refresh the statuses of project files

IntelliJ IDEA provides two refresh modes for statuses of files under Perforce control.

  * Standard Refresh takes into consideration only the changes made through the IntelliJ IDEA integration with Perforce. This improves performance as it does not require connecting to the server. However, this approach does not let you know about the changes made outside IntelliJ IDEA, for example, right through the p4v client application.

  * Force Refresh considers all the changes made to project, both from IntelliJ IDEA and from any other application, for example, right through p4v client.



  1. Open the Commit tool window `Alt+0`. 

  2. Do one of the following: 

     * To run Standard Refresh, click the Refresh toolbar button ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.refresh.svg) or press `Ctrl+F5`.

     * To run Force Refresh, click the Force Refresh toolbar button ![the Refresh button](https://resources.jetbrains.com/help/img/idea/2025.3/perforceChangesToolWindowForceRefresh.png).




29 August 2025

[Work with Perforce offline](perforce-working-offline.html)[Attach and detach Perforce jobs to changelists](attaching-and-detaching-perforce-jobs-to-changelists.html)
