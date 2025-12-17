[//]: # (Source: https://www.jetbrains.com/help/idea/creating-branches-and-tags.html)
[//]: # (Downloaded: 2025-12-17 19:23:28)

# Create Subversion branches and tags

IntelliJ IDEA allows you to create branches or tags on the basis of your local working copies, or their repository versions.

To create a branch or a tag in a Subversion repository, do the following:

  1. Go to VCS | Subversion | Branch or Tag. Alternatively, select the source folder in the [SVN Repositories tool window](svn-repositories.html) and choose the Branch or Tag command from the context menu.

  2. In the [Create Branch or Tag dialog](create-branch-or-tag-dialog-subversion.html) that opens, in the Copy From section, specify the source folder that will be copied to a branch or a tag. You can use your local working copy, or a repository location. 

If a repository location is selected as the source:

     * Click ![icon_idea.png](https://resources.jetbrains.com/help/img/idea/2025.3/icon_idea.png) to fill the Repository Location field with the path to the project location. 

     * Specify the revision to base the new branch on. This can be the HEAD revision, or a revision with the specified number. If the Specified option is selected, type the revision number, or click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and find the desired revision in the Subversion Changes Browser.

  3. In the Copy To section, specify the destination where the branch or the tag will be created. If you use the base URL, specify the name of the new branch or tag. If you opt to create a branch or tag in another repository location, type its URL, or click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and select the destination from the [Select Repository Location](select-repository-location-dialog-subversion.html) dialog.

  4. Optionally, enter a comment and click OK.




08 October 2024

[Configuring Subversion Branches](configuring-subversion-branches.html)[Export information from Subversion repository](exporting-information-from-subversion-repository.html)
