[//]: # (Source: https://www.jetbrains.com/help/idea/viewing-and-fast-processing-of-changelists.html)
[//]: # (Downloaded: 2025-12-17 20:06:18)

# View and fast process of changelists

If you are using Subversion 1.5 or later on the server and in your local working copy, you can take advantage of the extended Merge Info functionality implemented through the [Merge Info](version-control-tool-window-repository-and-incoming-tabs.html#mergeInfo) pane of the Version Control tool window `Alt+9`, the [Repository tab](version-control-tool-window-repository-and-incoming-tabs.html).

With this functionality, instead of browsing all changelists within a certain period, you can define a set of changelists to display. This is done by specifying a pair of branches in the repository (source and target), whereupon IntelliJ IDEA shows only the changelists from the source branch that have been integrated into the target branch.

Additionally, you can specify various filtering options to minimize the number of extraneous changelists.

Finally, integration and managing integration status are also available directly from the Merge Info pane.

The extended browsing functionality includes: 

If you are using SVN 1.4 or lower, to enable the Merge Info functionality, you need to [change the format of your local working copy](configuring-the-format-of-the-local-working-copy.html) first.

Before enabling the extended Merge Info functionality, make sure you are using SVN Server 1.5 or later.

08 April 2024

[Share directory](sharing-directory.html)[Define the set of changelists to display](defining-the-set-of-changelists-to-display.html)
