[//]: # (Source: https://www.jetbrains.com/help/idea/mq-project-name-tab.html)
[//]: # (Downloaded: 2025-12-17 19:32:52)

## Toolbar and Context Menu

Item| Shortcut| Description| Available from  
---|---|---|---  
![](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.refresh.svg)Reload from file| `Ctrl+F5`| Use this command to refresh the list of patches from the `series` file.Note that when you drag patches in the queue, the corresponding changes in the `series` file will only be saved when you switch to a different tab, or perform some other external action. This allows you to revert such changes by reloading from file.| Toolbar  
![mercurial_goto.png](https://resources.jetbrains.com/help/img/idea/2025.3/mercurial_goto.png)Goto| `Alt+Shift+G`| Use this command to apply the selected patch and all patches above it in the queue. The applied patches will become visible in the [Log tab](log-tab.html) and the changes will be registered in the working copy of the repository.| ToolbarContext menu  
Move and Push| `Alt+Shift+P`| Use this command to apply the selected patch without applying whatever other patches may be before it in the patch stack.| ToolbarContext menu  
![mercurial_fold.png](https://resources.jetbrains.com/help/img/idea/2025.3/mercurial_fold.png)Fold| `Alt+Shift+D`| Use this command to merge the selected non-applied patch with the topmost applied patch, and remove it from the list.| ToolbarContext menu  
![the Delete button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.gc.svg)Delete| `Delete`| Use this command to delete the selected patch from the series file| Toolbar  
Apply Patch| N/A| Use this command to apply the selected patch. The Apply Patch dialog will be displayed where you can select which changes you want to restore.| Context menu
