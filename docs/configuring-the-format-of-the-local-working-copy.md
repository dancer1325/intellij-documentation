[//]: # (Source: https://www.jetbrains.com/help/idea/configuring-the-format-of-the-local-working-copy.html)
[//]: # (Downloaded: 2025-12-17 19:22:08)

# Configure the format of the local working copy

A working copy is a directory that contains a collection of files which you can use as your private work area, as well as some extra files, created and maintained by Subversion. For example, each directory in your working copy contains an administrative directory named .svn.

You can have local working copies created with Subversion 1.3, 1.4, 1.5, 1.6, 1.7, 1.8, or 1.9. IntelliJ IDEA handles all these formats, giving you a choice to upgrade to the new format or preserve the legacy one.

Switching to another Subversion format is always associated with a specific working copy (directory) under the Subversion control. In other words, one cannot upgrade to a newer Subversion format at the IDE level, but only to a directory under Subversion control.

To check VCS association, go to [File | Settings | Version Control](settings-version-control.html) where all mappings between the project directories (or the entire project) and VCSs are listed.

To change the format of the local working copy, do the following:

  1. Open the Subversion tool window `Alt+9`.

  2. In the Subversion tool window `Alt+9`, switch to the [Subversion Working Copies Information](subversion-working-copies-information-tab.html) tab. 

This tab is only available, when the current project sources are entirely or partially under Subversion control.

  3. Scroll to the information on the required directory and click the Change link. 

Note that Subversion 1.9 can be used with the local working copy version 1.8, so in this case the Change link will not appear.

  4. In the Convert Working Copy Format dialog, that opens, select the desired format option.




11 February 2024

[Compare with branch in Subversion](comparing-with-branch.html)[Configure HTTP proxy in Subversion](configuring-http-proxy.html)
