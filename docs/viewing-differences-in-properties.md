[//]: # (Source: https://www.jetbrains.com/help/idea/viewing-differences-in-properties.html)
[//]: # (Downloaded: 2025-12-17 20:06:21)

# View differences in properties

With IntelliJ IDEA, you can view differences in properties between a file in the [local copy and in the repository](#localAndRepository) or between [two revisions](#revisions) of a file in the local copy.

### To view property difference between the local copy and the repository version

  1. Open the Version Control tool window and switch to the [Repository](version-control-tool-window-repository-and-incoming-tabs.html) tab.

  2. In the [Changed Files](version-control-tool-window-repository-and-incoming-tabs.html#right) pane, select the file for which you want to view property differences.

  3. Choose Properties Diff From the context menu of the selection or click ![propertiesDiff.png](https://resources.jetbrains.com/help/img/idea/2025.3/propertiesDiff.png) on the toolbar. 

![showDiffLocalRepository.png](https://resources.jetbrains.com/help/img/idea/2025.3/showDiffLocalRepository.png)
  4. In the Subversion properties difference viewer, explore the differences: 

![svnPropertiesDiffRemoteResults.png](https://resources.jetbrains.com/help/img/idea/2025.3/svnPropertiesDiffRemoteResults.png)



### To view property difference between two revisions in the local copy

  1. Open the Commit tool window `Alt+0`. 

  2. Select the file for which you want to view property differences between revisions and choose Subversion | Properties Diff with Local in the context menu. 

![showPropertiesDiffLocal.png](https://resources.jetbrains.com/help/img/idea/2025.3/showPropertiesDiffLocal.png)
  3. In the Subversion properties difference viewer explore the differences: 

![svnPropertiesDiffLocalResults.png](https://resources.jetbrains.com/help/img/idea/2025.3/svnPropertiesDiffLocalResults.png)



08 October 2024

[Work with Subversion properties for files and directories](working-with-subversion-properties-for-files-and-directories.html)[Resolve property conflicts](resolving-property-conflicts-svn.html)
