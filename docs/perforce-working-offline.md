[//]: # (Source: https://www.jetbrains.com/help/idea/perforce-working-offline.html)
[//]: # (Downloaded: 2025-12-17 19:33:50)

# Work with Perforce offline

The Perforce plugin keeps a log of VCS operations performed while offline, and replays the log when the user comes back online. The log of operations is stored in the .iws file and persists between IntelliJ IDEA restarts.

While offline, you can perform the following operations, which will be automatically replayed in online mode:

  * Edit

  * Add/Copy

  * Delete

  * Move/Rename

  * Revert

  * Move to another changelist

  * View Committed/Incoming changes (displaying cached information only).




The following operations are not supported in offline mode: update, commit, integrate, tracking of the unversioned, locally deleted and _modified without checkout_ files (unversioned files are shown as _unchanged_), and any other operations that require server connection.

The performance of IntelliJ IDEA Perforce integration in offline mode is considerably better than in online mode (because no server calls are required), so you might want to use offline mode even though connection to the Perforce server is successful.

### Go to offline mode

When offline mode is activated, the following notification balloon appears:

![Perforce is offline notification](https://resources.jetbrains.com/help/img/idea/2025.3/perforceOffline1.png)

This balloon fades after a while; Perforce is offline message appears at the bottom of the Local Changes tab of the Perforce tool window.

  * Automatically, when the Perforce server becomes unavailable. IntelliJ IDEA switches to the offline mode automatically, and displays an offline notification in a popup. To enable this behaviour, select the Switch to offline mode automatically if Perforce is unavailable checkbox in the [Perforce](settings-version-control-perforce.html) page of the [Settings](settings-preferences-dialog.html) dialog.

  * Manually at anytime, by choosing VCS | Perforce and select Work Offline From the context menu.




### Return to online mode

  * Choose VCS | Perforce and clear Work Offline.

  * In the offline notification balloon, click the Go online link.

  * In the Commit window, click the Go online link: 

![perforceOffline2.png](https://resources.jetbrains.com/help/img/idea/2025.3/perforceOffline2.png)



14 May 2025

[Use multiple Perforce depots with P4CONFIG](using-multiple-perforce-depots-with-p4config.html)[Check Perforce project status](checking-perforce-project-status.html)
