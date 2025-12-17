[//]: # (Source: https://www.jetbrains.com/help/idea/settings-file-colors.html)
[//]: # (Downloaded: 2025-12-17 20:01:06)

## Configure colors

Similarly to scopes, color associations can be local and shared.

  * Local colors are only visible to you and are not shared through VCS.

  * Shared colors are placed under version control so that people who work on a project can use the same color associations. They are stored in the project folder under .idea in the fileColors.xml file (for example: MyProject/.idea/fileColors.xml).




Item| Tooltip| Description  
---|---|---  
![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)| Add| Open a list with the available scopes. Click ![the right arrow button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.arrowRight.svg) next to the necessary scope in the list and select a color.  
![the Remove button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)| Remove| Remove the selected color-scope association.  
![the Move up button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moveUp.svg)/![the Move down button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.moveDown.svg)| Up / Down| Sort the color-scope associations and [change the order](configuring-scopes-and-file-colors.html#arrange-the-order-of-scopes) in which they are applied.  
Share through VCS| | Share the selected local scope through VCS.  
  
Apply the changes and close the dialog. After that you will see colors in the selected areas in the interface:

![Scope highlighting in the editor tabs and search results](https://resources.jetbrains.com/help/img/idea/2025.3/ij_scope_highlighting.png)

This topic explains how to set colors distinguishing project files of specific scopes. If you need to set VCS file status colors, refer to [this page](adding-files-to-version-control.html#file_status).
