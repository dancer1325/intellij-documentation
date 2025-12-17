[//]: # (Source: https://www.jetbrains.com/help/idea/edit-jobs-linked-to-changelist-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:25:26)

# Edit Jobs Linked to Changelist dialog

The dialog opens in the following cases:

  * When you select a changelist and then select Edit Associated Jobs from the context menu.

  * When you click the ![icon_openLocalVersion.png](https://resources.jetbrains.com/help/img/idea/2025.3/icon_openLocalVersion.png) button in the Perforce area of the Commit Changes dialog.




Use the dialog to search for Perforce jobs, link jobs to the selected changelist, and detach currently linked jobs.

Item| Tooltip and Shortcut| Description  
---|---|---  
![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)| Unlink selected jobs| Click this button to detach the selected job from the changelist.  
![findPerforceJob.png](https://resources.jetbrains.com/help/img/idea/2025.3/findPerforceJob.png)| Search| Click this button to open the [Link Job to Changelist](link-job-to-changelist-dialog.html) dialog, where you can search for available jobs, view their details, and link the desired job to the changelist.  
![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)| Find and link job matching the pattern| Click this button to start quick search for the job that matches the pattern specified in the field and attach the job to the changelist.In the field, specify the exact name of the desired job or a search pattern according to the Perforce jobs [syntax rules](http://www.perforce.com/perforce/doc.081/manuals/cmdref/jobs.html#1040665).  
If only one job matching the pattern is found, it is attached to the changelist automatically. Otherwise, to select a job among several available jobs, click ![findPerforceJob.png](https://resources.jetbrains.com/help/img/idea/2025.3/findPerforceJob.png) and find the desired job using the [Link Job to Changelist](link-job-to-changelist-dialog.html) dialog.  
Close| Click this button to save the specified settings and leave the dialog.  
  
30 September 2025

[Attach and detach Perforce jobs to changelists](attaching-and-detaching-perforce-jobs-to-changelists.html)[Integrate File dialog (Perforce)](integrate-file-dialog-perforce.html)
