[//]: # (Source: https://www.jetbrains.com/help/idea/settings-version-control-directory-mappings.html)
[//]: # (Downloaded: 2025-12-17 20:02:21)

# Directory Mappings

In this page, specify which [version control systems](version-control-integration.html) will be used for specific directories or the entire project.

Item| Description  
---|---  
Directory| This field shows the path to project directories or the project roots.For projects with Git or Mercurial integration enabled, IntelliJ IDEA scans project directories to check if there are Git or Mercurial repositories that are not controlled by the IDE. If such repositories are found, they are listed here under Unregistered roots and are marked grey. To add an unregistered root, select it in the list and click the Add button ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg).IntelliJ IDEA also checks if registered roots are valid, in other words, that a Git or Mercurial repository exists at the specified path. If invalid repositories are detected, they are marked with red.  
VCS| Select a version control system for the specified directory.VCS integration in IntelliJ IDEA is provided through a set of bundled [plugins](managing-plugins.html) enabled by default. So the list only displays the version control systems which plugins are enabled.  
![Add](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)| Click this button to add a directory mapping to the list. The Add VCS Directory Mapping dialog opens where you can specify the required directory, select a VCS for it, and open the Version Control Configurations dialog to configure the specified VCS, if necessary. If you have a project with multiple version control systems, select `<Project>` instead of `Directory` to apply mapping to content roots of all modules and all first-level directories of your project.  
![Edit](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.edit.svg)| Click this button to edit the selected directory mapping. The Edit VCS Directory Mapping dialog opens where you can update the selected mapping and configure the specified VCS, if necessary.   
![Remove](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)| Click this button to remove the selected directory mapping from the list.  
  
17 June 2025

[Commit](commit-dialog.html)[Confirmation](settings-version-control-confirmation.html)
