[//]: # (Source: https://www.jetbrains.com/help/idea/settings-tools-external-diff-tools.html)
[//]: # (Downloaded: 2025-12-17 20:01:58)

# External Diff Tools

Specify external tools for comparing or merging files and folders, and associated settings.

![External Diff Tools dialog in Settings](https://resources.jetbrains.com/help/img/idea/2025.3/settings_external_diff_merge.png)

Item| Description  
---|---  
Enable external tools| Select to use an external tool to compare or merge files or folders.  
Configure external tools  
![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)| Add a new external tool. In the dialog the opens, configure the following options:

  * Tool group: select whether you want to use a diff or merge tool.
  * Program path: specify the path to the executable file of the tool you want to use.For example: C:\Program Files\Beyond Compare 4\BCompare.exe on Windows or /Applications/Beyond Compare.app/Contents/MacOS/bcomp on macOS.
  * Tool name: enter the name of the external tool that you're configuring.
  * Argument pattern: set the diff tool parameters.Specify the necessary parameters in the proper order:
    * %1: left (local changes)
    * %2: right (server changes)
    * %3: base (the current version without the local changes)
    * (merge tool only) %4: output (merge result)
  * (merge tool only) Trust process exit code: select to silently finish the merge if the `exitCode` of the external merge tool is set to `0` (successful). Otherwise, you will be prompted to indicate the success of the resolution after the tool has exited.

![Configuring external diff tool](https://resources.jetbrains.com/help/img/idea/2025.3/external-diff-merge.png)  
![Remove](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)| Remove the selected external tool.  
![the Edit button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.edit.svg)| Edit the settings of the selected external tool.  
Configure external diff/merge tools associated with a file type  
![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)| Add a file type and configure the diff and external tool that will be used to process files of this type.  
![Remove](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)| Remove the selected association between a file type and an external diff or merge tool.  
  
20 June 2025

[Diff & Merge](settings-tools-diff-and-merge.html)[Jupyter](jupyter-settings.html)
