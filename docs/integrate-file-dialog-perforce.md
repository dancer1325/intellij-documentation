[//]: # (Source: https://www.jetbrains.com/help/idea/integrate-file-dialog-perforce.html)
[//]: # (Downloaded: 2025-12-17 19:29:40)

# Integrate File dialog (Perforce)

Use this dialog to integrate changelists from one branch spec to another.

Item| Description  
---|---  
Branch Spec| Select the branch spec that will be used for change integration. Consider the following: 

  * If the Reverse option is enabled, changes are integrated from the selected branch to the local copy.
  * If the Reverse option is disabled, changes are integrated from the local copy to the selected branch.

  
Integrate changelist| Use this option to invoke the Changes Browser, where you can select the changelist that will be integrated into the current branch/local copy.  
Store Changes To Changelist| Specify the changelist where the integrated changes should be stored.  
Revert unchanged files before sync (p4 revert -a)| Select this option to revert unchanged files.  
Run resolve automatically after the sync (p4 resolve -am)| Select this option to automatically resolve the files that can be resolved without conflicts.  
  
14 May 2025

[Edit Jobs Linked to Changelist dialog](edit-jobs-linked-to-changelist-dialog.html)[Link Job to Changelist dialog](link-job-to-changelist-dialog.html)
