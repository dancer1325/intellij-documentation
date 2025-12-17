[//]: # (Source: https://www.jetbrains.com/help/idea/workspaces.html)
[//]: # (Downloaded: 2025-12-17 20:07:37)

## Creating a workspace

You can create an empty workspace or create one with projects either from the IntelliJ IDEA welcome screen or from within the IDE.

### Create a new workspace from the Welcome screen

  1. Launch the [New Project wizard](new-project-wizard.html). If no project is currently opened in IntelliJ IDEA, click New Project on the welcome screen. Otherwise, select File | New | Project from the main menu.

  2. Name the new workspace and change its location if necessary.

  3. Select the Create Git repository to place the new workspace under version control. Since the workspace is a file that contains only references to your projects, this action creates a Git repository only for the workspace.

You will be able to do it later at any time.

The `.gitignore` file is generated in any case.

  4. Click Create to create an empty workspace, or under the Workspace Projects section, click ![the Add icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) or the Add Projects link to add projects from your local file system to the workspace and then click Create.

![Workspace projects](https://resources.jetbrains.com/help/img/idea/2025.3/workspace_projects.png)

IntelliJ IDEA opens the created workspace with the attached projects.




### Create a workspace from inside the IDE

  1. From the main menu, select File | Open.

  2. In your local file system, select projects you want to combine into one workspace and click Open.

  3. In the notification dialog that opens, click Yes.

  4. In the New Workspace dialog, add the name and location of your workspace and click OK. 

![New Workspace](https://resources.jetbrains.com/help/img/idea/2025.3/new_workspace_several_projects.png)

IntelliJ IDEA opens the workspace in the IDE with selected projects.



