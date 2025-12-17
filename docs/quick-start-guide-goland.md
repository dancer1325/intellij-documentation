[//]: # (Source: https://www.jetbrains.com/help/idea/quick-start-guide-goland.html)
[//]: # (Downloaded: 2025-12-17 19:56:39)

## Start a Go project

After you install the Go plugin and launch it for the first time, you need to create a project. Everything in IntelliJ IDEA is done within the context of a project. A project serves as the foundation for code assistance, refactoring, consistent coding style, and other key features.

You have three options to start working on a project in the IDE:

  * Open an existing project

  * Check out a project from a version control system (VCS)

  * Create a new project




This quick start guide covers only how to create a new project.

### Create a Go project

  1. Select File | New | New Project. 

Alternatively, navigate to New | Project on the Welcome to IntelliJ IDEA dialog.

  2. In the New Project dialog, select Go modules from the list of available project types.

Ensure that Go is selected as the project language in the Language list.

  3. In the GOROOT field, specify the location of your Go installation. IntelliJ IDEA usually detects this location automatically.

To change or install a new Go SDK version, click Add SDK (![Add SDK icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg)) and choose one of the following options:

     * Local: to use an existing SDK from your local system.

     * Download: to download a Go SDK version from the official repository.

  4. Click Create to create the project.

![Download Go SDK](https://resources.jetbrains.com/help/img/idea/2025.3/go_ij_create_go_modules_project.png)



### Create a Go file

  1. To create a Go file, use one of the following options:

     * In the Project tool window, right-click the parent folder of your project and select New | Go FileGo File.

     * Click the parent folder of your project, press `Alt+Insert`, and select Go File.

     * Click the parent folder of your project, then go to File | New | Go File.

  2. In the New Go File dialog, enter a file name and choose the file type:

     * Empty file — creates an empty Go file.

     * Simple application — creates a Go file with a predefined `main` function.

![Create a Go file](https://resources.jetbrains.com/help/img/idea/2025.3/go_ij_qst_create_go_file.png)


