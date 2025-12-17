[//]: # (Source: https://www.jetbrains.com/help/idea/create-branch-or-tag-dialog-subversion.html)
[//]: # (Downloaded: 2025-12-17 19:22:54)

# Create Branch or Tag dialog (Subversion)

In this dialog, set the arguments for creating a branch or a tag on the basis of a local working copy or a repository version.

Item| Description  
---|---  
Copy from| In this section, specify the source folder to create a branch or tag from. The source of the copy can be taken from the local working copy or from the repository.  
Working Copy| Click this option to create a branch or tag on the basis of your local working copy. Type the path in the field or click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and select the desired directory in the dialog that opens.  
Repository Location| Click this option to create a branch or tag on the basis of the repository. Do one of the following: 

  * Type the URL of the repository location in the field.
  * Click the browse button and select the source repository location.
  * Click the ![IDEA.gif](https://resources.jetbrains.com/help/img/idea/2025.3/IDEA.gif) button to use the project home directory.

  
Revision| In this section, specify the source revision to create a branch or tag from. The available options are: 

  * HEAD \- select this option to have a branch or tag created on the basis of the HEAD revision.
  * Specified \- select this option to have a branch or tag created on the basis of a specific revision. Type the revision number in the field manually or click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and select the desired revision in the Changes Browser dialog, that opens.

  
Copy to| Use this section to define the target folder for a branch or tag. The available options are:

  * Branch or Tag \- select this option to have the selected revision copied to a specific branch or tag. In the Base URL field, specify the base URL of the branch or tag. In the Name field, specify the name of the new branch.
  * Any location \- select this option to have the selected revision copied to a location of your choice. In the field below, specify the URL of any valid location. Type the URL manually or click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and specify the desired location in the Select Repository Location dialog, that opens.

  
Comment| Type some meaningful description in the text area.  
Switch to the newly created branch or tag| Select to jump to the branch or tag you've created.  
  
08 October 2024

[Configure Subversion Branches](configure-subversion-branches.html)[Import into Subversion](import-into-subversion.html)
