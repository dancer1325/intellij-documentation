[//]: # (Source: https://www.jetbrains.com/help/idea/working-with-git-tutorial.html)
[//]: # (Downloaded: 2025-12-17 20:07:25)

## Step 1. Create a new project with a Git repository

In this tutorial, we will create a simple project, share it on GitHub, and perform some Git tasks.

  1. Launch IntelliJ IDEA and click New Project on the Welcome screen.

If you have another project open in IntelliJ IDEA at the moment, select File | New Project from the main menu.

  2. In the dialog that opens, select the project type (for this tutorial, we will create just an Empty Project), specify the name of the project (for example, `gitdemo`), and provide the location path. 

Select the Create Git repository checkbox.

![%alt_new_project](https://resources.jetbrains.com/help/img/idea/2025.3/gitdemo_empty_project.png)

Click Create. The new project will open in IntelliJ IDEA.

IntelliJ IDEA automatically detects if Git is installed on your computer. If the IDE cannot locate a Git executable, it suggests downloading it.




You will get a notification that the local Git repository has been created for your project. Also, dedicated tool windows for working with Git become available.

![Git integration enabled](https://resources.jetbrains.com/help/img/idea/2025.3/git_integration_enabled.png)

  1. Git Branches popup: [manage Git branches](manage-branches.html) and perform basic Git operations.

  2. Commit tool window (`Ctrl+K` or View | Tool Windows | Commit): [review the local changes](adding-files-to-version-control.html) and [commit](#commit_and_push) them to the local Git repository.

  3. Git tool window (`Alt+9` or View | Tool Windows | Git): [work with the Git log](investigate-changes.html) and [more](version-control-tool-window.html).



