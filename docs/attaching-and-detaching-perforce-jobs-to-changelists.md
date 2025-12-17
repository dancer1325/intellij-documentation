[//]: # (Source: https://www.jetbrains.com/help/idea/attaching-and-detaching-perforce-jobs-to-changelists.html)
[//]: # (Downloaded: 2025-12-17 19:18:35)

# Attach and detach Perforce jobs to changelists

The Perforce integration with IntelliJ IDEA provides you with a user interface for attaching and detaching Perforce [jobs](http://www.perforce.com/perforce/doc.081/manuals/cmdref/jobs.html) to changelists.

Note that the integration does not support creation of Perforce jobs.

To get access to working with Perforce jobs, select the Enable Perforce Jobs Support checkbox on the [Perforce](settings-version-control-perforce.html) page of the [Settings](settings-preferences-dialog.html) dialog.

From this topic you will learn how to:

  * Attach jobs to changelists: 

    * [At any stage](#local) of your work from the Commit window.

    * [During commit](#commit) from the Commit Changes dialog.

  * Find the desired job to attach to a changelist using: 

    * The [standard search](#standardSearch) functionality, which enables you to specify numerous search criteria and thus to flexibly configure the search procedure.

    * The [quick search](#quickSearch) functionality, which enables you to have the found job linked to the changelist automatically.

  * [Detach](#detach) jobs from changelists.




Quick search is helpful when you need to attach only one job to a changelist and you either know the exact name of the desired job or at least can specify a search pattern for the name.

### To find and link a job at any stage of your work

  1. Open the Commit tool window `Alt+0`. 

  2. Select the changelist you want to link a job to.

  3. From the context menu of the changelist, choose Edit Associated Jobs.

  4. Find the desired job. Do one of the following: 

     * To use the [standard search](#standardSearch) functionality, click the ![findPerforceJob.png](https://resources.jetbrains.com/help/img/idea/2025.3/findPerforceJob.png) button.

     * To use the [quick search](#quickSearch) functionality, click the ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) button.

  5. View the details of the found job and click OK.




### To find and link a job during commit

  1. In the Commit window, select the changelist you want to link a job to and open the Commit Changes dialog. 

  2. Find the desired job using the controls in the Jobs area. Do one of the following:

     * To use the [standard search](#standardSearch) functionality, click the ![findPerforceJob.png](https://resources.jetbrains.com/help/img/idea/2025.3/findPerforceJob.png) button.

     * To use the [quick search](#quickSearch) functionality, click the ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) button.

  3. View the details of the found job and continue the commit procedure.




### To find a job using the standard search functionality

  1. In the dialog that opens or in the Jobs area of the Commit Changes dialog, click the ![findPerforceJob.png](https://resources.jetbrains.com/help/img/idea/2025.3/findPerforceJob.png) button.

Which dialog you are currently in depends on whether you are linking jobs [during commit](#commit) or at any [other stage](#local) of work.

  2. In the dialog that opens, specify the desired search parameters.

At least one of the fields should be filled in.

  3. Click the Search button. The jobs that match the specified criteria are shown in the Search Results list. To view the details of a job, select it in the list.

  4. Select the desired job and click OK. The dialog closes, and you return to the dialog where you started the search:

     * The Commit Changes dialog, if you are linking jobs [during commit](#commit).

     * The Edit Jobs Linked to Changelist dialog, if you are linking jobs at any [other stage](#local) of work.




### To quickly find and link one job

  1. Open the Edit Jobs Linked to Changelist dialog or switch to the Jobs area of the Commit Changes dialog. 

The dialog to be used depends on whether you are linking jobs [during commit](#commit) or at any [other stage](#local) of work.

  2. In the field, type the desired job name search pattern and click the ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) button. The job is found and automatically linked to the current changelist. 

If no job matching the specified pattern is found, the corresponding information message is displayed.

The details of jobs that are found and linked through the quick search functionality are available only in the Edit Jobs Linked to Changelist dialog.




### To detach a job from a changelist

  * In the Edit Jobs Linked to Changelist dialog or in the Jobs area of the Commit Changes dialog, select the desired job and click the ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg) button. 

The dialog to be used depends on whether you are detaching jobs [during commit](#commit) or at any [other stage](#local) of work.




30 September 2025

[Check Perforce project status](checking-perforce-project-status.html)[Edit Jobs Linked to Changelist dialog](edit-jobs-linked-to-changelist-dialog.html)
