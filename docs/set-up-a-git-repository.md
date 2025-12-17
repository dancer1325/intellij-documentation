[//]: # (Source: https://www.jetbrains.com/help/idea/set-up-a-git-repository.html)
[//]: # (Downloaded: 2025-12-17 20:00:14)

## Check out a project from a remote host (git clone)

IntelliJ IDEA allows you to check out (in Git terms, clone) an existing repository and create a new project based on the data you've downloaded.

  1. To start cloning a Git repository, do one of the following:

     * If the version control integration is already enabled, go to Git | Clone.

     * If the version control integration is not enabled yet, go to VCS | Get from Version Control.

Alternatively, go to File | New | Project from Version Control.

     * If no project is currently open, click Clone Repository on the Welcome screen.

  2. In the Clone Repository dialog, specify the URL of the remote repository you want to clone or select one of the VCS hosting services on the left.

If you are already logged in to the selected hosting service, completion will suggest the list of available repositories that you can clone.

![Getting a project from GitHub](https://resources.jetbrains.com/help/img/idea/2025.3/get-from-vc-git.png)

If you want to perform [shallow clone](https://git-scm.com/docs/git-clone#Documentation/git-clone.txt-code--depthcodeemltdepthgtem) with a limited history, select the Shallow clone with a history truncated to checkbox and specify the number of commits that you want to clone.

You can fetch the rest of the history later by selecting Git | Unshallow Repository in the main menu.

  3. Click Clone. If you want to create a project based on the sources you have cloned, click Yes in the confirmation dialog. Git root mapping will be automatically set to the project root directory.

If your project contains [submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules), they will also be cloned and automatically registered as project roots.

  4. In the Trust and Open Project '<project_name>'? [project security dialog](project-security.html), select the way you want to open the project: Trust Project or Preview in Safe Mode.

  5. When you import or clone a project for the first time, IntelliJ IDEA analyzes it. If the IDE detects more than one configuration (for example, Eclipse and Gradle), it prompts you to select which configuration you want to use.

If the project that you are importing uses a build tool, such as [Maven](maven-support.html) or [Gradle](gradle.html), we recommend that you select the build tool configuration.

Select the necessary configuration and click OK.

![Dialog that prompts you to select how you want to import the project](https://resources.jetbrains.com/help/img/idea/2025.3/import-from-providers.png)

The IDE pre-configures the project according to your choice. For example, if you select Gradle, IntelliJ IDEA executes its build scripts, loads dependencies, and so on.



