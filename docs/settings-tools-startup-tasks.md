[//]: # (Source: https://www.jetbrains.com/help/idea/settings-tools-startup-tasks.html)
[//]: # (Downloaded: 2025-12-17 20:02:12)

# Startup Tasks

On this page, create a list of run/debug configurations to be launched automatically on the project start. This may be helpful if you run some Grunt or Gulp.js tasks or npm scripts on a regular basis. All you need is just add the run/debug configurations that launch such tasks or scripts to the list of startup tasks.

Item| Tooltip| Description  
---|---|---  
Run Configuration| This read-only field shows the names of the run configurations to be launched on the project start.  
Shared| When this checkbox is selected, the corresponding task is available for other team members. Note that you can share only those run configurations that are already marked as shared in their definitions. If the [directory-based project format](creating-and-managing-projects.html#project-formats) is used, the settings for a run/debug configuration are stored in a separate .xml file in the .idea\runConfigurations folder if the run/debug configuration is shared, or in the .idea\workspace.xml file otherwise.If the [file-based format](creating-and-managing-projects.html#project-formats) is used, the settings are stored in the .ipr file for shared configurations, or in the .iws file otherwise.  
![Add](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)| Add| Click this button to add one of the run/debug configurations that are currently defined in the project to the list of tasks to be executed on the project start. Choose the relevant configurations from the list or choose Edit Configurations to open the [Run/debug configurations dialog](run-debug-configurations-dialog.html) dialog and define a required configuration in it.  
![Remove](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)| Remove| Click this button to delete the selected task from the list.  
![Edit](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.edit.svg)| Edit| Click this button to open the [Run/debug configurations dialog](run-debug-configurations-dialog.html) dialog with the settings from the selected configuration and update them as required.  
  
03 September 2025

[Settings Repository](settings-tools-settings-repository.html)[Vagrant](vagrant.html)
