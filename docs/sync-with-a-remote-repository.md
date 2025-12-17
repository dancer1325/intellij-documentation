[//]: # (Source: https://www.jetbrains.com/help/idea/sync-with-a-remote-repository.html)
[//]: # (Downloaded: 2025-12-17 20:03:48)

## Fetch changes

When you fetch changes from the upstream, all new data from commits that were made since you last synced with the remote repository is downloaded into your local copy. This new data is not integrated into your local files, and changes are not applied to your code.

Fetched changes are stored as a remote branch, which gives you a chance to review them before you [merge](apply-changes-from-one-branch-to-another.html#merge) them with your files. Since fetch does not affect your local development environment, this is a safe way to get an update of all changes to a remote repository.

There are two ways to fetch changes from the upstream:

  * Select Git | Fetch in the main menu.

  * Alternatively, open the Branches popup and click ![the Fetch icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.vcs.fetch.svg) in the upper right corner. 

![Fetch icon in branches popup](https://resources.jetbrains.com/help/img/idea/2025.3/VCS_fetch_from_branches_popup.png)



[Watch this video](https://youtu.be/tnz2I9rxrfk) to get a better view on how fetch operation is performed in IDE.
