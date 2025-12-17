[//]: # (Source: https://www.jetbrains.com/help/idea/resolving-conflicts-with-perforce-integration.html)
[//]: # (Downloaded: 2025-12-17 19:57:38)

# Resolve conflicts with Perforce integration

The conflicts might occur in course of team work. Perforce integration makes use of the following commands:

  * Resolve enables you to resolve a conflict to a specific file.

  * Resolve All applies to all files in a changelist that have merge status.




### To resolve conflicts for the files under Perforce version control

  1. In the Commit window, select a conflicting file, or a whole conflict node.

  2. From the context menu of the selection, choose Resolve or Resolve All. The Conflicts dialog appears.

  3. If you want to accept the server version and overwrite your local changes, click Accept Theirs. If you want to force your changes to the repository, click Accept Yours. Clicking Merge opens the merge tool, where you can accept or discard each change individually.

  4. Once the conflicts are successfully resolved, commit your local version to the repository.




14 May 2025

[Integrate Perforce files](integrating-perforce-files.html)[Show Revision Graph and Time-Lapse View](showing-revision-graph-and-time-lapse-view.html)
