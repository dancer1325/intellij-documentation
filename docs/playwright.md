[//]: # (Source: https://www.jetbrains.com/help/idea/playwright.html)
[//]: # (Downloaded: 2025-12-17 19:33:58)

## Create a new Playwright project

  1. In the main menu, go to File | New | Project.

Alternatively, if you're on the Welcome screen, click New Project.

  2. From the list on the left, select Playwright. 

![Creating a new Playwright project](https://resources.jetbrains.com/help/img/idea/2025.3/ij_playwright_new_project.png)
  3. Name the new project and change its location if necessary.

  4. Specify the Node.js runtime.

  5. Specify the command to install Playwright.

  6. Click Create.




  1. In the main menu, go to File | New | Project.

Alternatively, if you're on the Welcome screen, click New Project.

  2. From the list on the left, select Playwright for JVM. 

![Creating a new Playwright for JVM project](https://resources.jetbrains.com/help/img/idea/2025.3/ij_create_playwright_jvm_project.png)
  3. Name the new project and change its location if necessary.

  4. (Optional) Enable the Create Git repository option to place the new project under version control. If you do not want to do it now, you can do it later at any time.

  5. Select the Language that you want to use.

  6. Select the build system that you want to use in your project: [Maven](maven-support.html) or [Gradle](gradle.html).

  7. Select the test framework that you want to use for test cases management: [JUnit](junit.html) or [TestNG](testng.html).

  8. (Optional) Modify the Group and Artifact parameters.

  9. From the JDK list, select the [JDK](sdk.html#jdk) that you want to use in your project.

If the JDK is installed on your computer, but not defined in the IDE, select Add JDK and specify the path to the JDK home directory.

If you don't have the necessary JDK on your computer, select Download JDK.

  10. (Optional) Enable the Add sample code parameter.

  11. Click Next.

  12. Click Create.




The Playwright for Python project can be created only if the [Python plugin](https://plugins.jetbrains.com/plugin/631-python) is [installed and enabled](managing-plugins.html).

  1. In the main menu, go to File | New | Project.

Alternatively, if you're on the Welcome screen, click New Project.

  2. From the list on the left, select Playwright for Python. 

![Creating a new Playwright for Python project](https://resources.jetbrains.com/help/img/idea/2025.3/ij_playwright_python_virtualenv.png)
  3. Name the new project and change its location if necessary.

  4. (Optional) Enable the Create Git repository option to place the new project under version control. If you do not want to do it now, you can do it later at any time.

  5. Select whether you want to create a new or use an existing Environment and configure the corresponding settings. 

![Configure a new Virtualenv environment](https://resources.jetbrains.com/help/img/idea/2025.3/ij_playwright_python_virtualenv.png)
     * Select the base interpreter from the list, or click ![Choose the base interpreter](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) and find the Python executable in your file system.

     * Specify the location of the new virtual environment in the Location field, or click ![Virtual environment location](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) and browse for the location in your file system. The directory for the new virtual environment should be empty.

     * Select the Inherit packages from base interpreter checkbox if you want all packages installed in the global Python on your machine to be added to the virtual environment you're going to create. This checkbox corresponds to the `--system-site-packages` option of the [virtualenv](http://www.virtualenv.org/en/latest/index.html) tool.

     * Select the Make available to all projects checkbox if you want to reuse this environment when creating Python interpreters in IntelliJ IDEA.

For more information, refer to the [PyCharm documentation](https://www.jetbrains.com/help/pycharm/creating-virtual-environment.html).

![Configure a new Conda environment](https://resources.jetbrains.com/help/img/idea/2025.3/ij_playwright_python_conda.png)
     * Specify the location of the new conda environment in the Location field, or click ![Browse...](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) and browse for the location in your file system. The directory for the new conda environment should be empty.

     * Select the Python version from the list.

     * IntelliJ IDEA will detect a conda installation.

If IntelliJ IDEA did not detect the installation automatically, specify the location of the conda executable, or click ![Conda executable location](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) to browse for it.

     * Select the Make available to all projects checkbox if you want to reuse this environment when creating Python interpreters in IntelliJ IDEA.

For more information, refer to the [PyCharm documentation](https://www.jetbrains.com/help/pycharm/conda-support-creating-conda-virtual-environment.html).

![Configure a new Pipenv environment](https://resources.jetbrains.com/help/img/idea/2025.3/ij_playwright_python_pipenv.png)
     * Select the base interpreter from the list, or click ![Browse...](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) and find the Python executable in your file system.

     * If you have added the base binary directory to your `PATH` environmental variable, you do not need to set any additional options: the path to the pipenv executable will be autodetected.

If IntelliJ IDEA does not detect the pipenv executable, click Install pipenv via pip to allow IntelliJ IDEA to install it for you automatically.

Alternatively, follow the pipenv installation procedure to discover the executable path and then specify it in the dialog.

For more information, refer to the [PyCharm documentation](https://www.jetbrains.com/help/pycharm/pipenv.html).

![Configure a new Poetry environment](https://resources.jetbrains.com/help/img/idea/2025.3/ij_playwright_python_poetry.png)
     * Select the base interpreter from the list or click ![Browse...](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) and find the Python executable in your file system.

For more information, refer to the [PyCharm documentation](https://www.jetbrains.com/help/pycharm/poetry.html).

![Configure an existing environment](https://resources.jetbrains.com/help/img/idea/2025.3/ij_playwright_python_existing_env.png)
     * Select the interpreter from the list. If there are no available interpreters, click Add Interpreter and configure one according to your needs.

  6. Click Create.




A new project is created according to the options that you have selected.
