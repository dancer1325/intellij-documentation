[//]: # (Source: https://www.jetbrains.com/help/idea/indexing.html)
[//]: # (Downloaded: 2025-12-17 19:29:27)

## Viewing the indexing process

The right part of the status bar shows the progress of the indexing process. You may select Show all to view the specific tasks in the Backround Tasks dialog.

![Indexing is in progress](https://resources.jetbrains.com/help/img/idea/2025.3/index_show_all.png)

There are two main background tasks that are part of the indexing process: Scanning files to index and Updating indexes.

![Indexing is in progress](https://resources.jetbrains.com/help/img/idea/2025.3/ij_indexing_process_background_tasks.png)

There is no option to pause, resume, or cancel the Scanning files to index process. However, you may pause and resume the Updating indexes process. You cannot cancel it, though.

In order to have access to smart IDE functionality such as code completion and smart navigation, the Updating indexes process must have completed. However, the Scanning files to index process can still be in progress because it does not interrupt the access to smart IDE functionality.
