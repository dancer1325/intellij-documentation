[//]: # (Source: https://www.jetbrains.com/help/idea/creating-empty-python-project.html)
[//]: # (Downloaded: 2025-12-17 19:23:32)

# Create a Python project

Make sure that the [Python plugin](https://plugins.jetbrains.com/plugin/631-python) is [installed and enabled](managing-plugins.html). The plugin implements all the features of [PyCharm](https://www.jetbrains.com/pycharm/), the standalone IDE for Python developers. For more information about the supported features, refer to the [PyCharm documentation](https://www.jetbrains.com/help/pycharm/).

  1. Go to File | New | Project or on the Welcome screen, click New Project.

  2. In the New Project dialog, select Python as a project type.

![New Python project: existing interpreter](https://resources.jetbrains.com/help/img/idea/2025.3/ij_python_sdk_existing_interpreter.png)

Specify the project location. The project name will be automatically derived from the folder name in the specified path.

  3. If you want to proceed with the Project venv, uv or Base conda interpreter, select the corresponding option and click Create.

Project venv
    

IntelliJ IDEA creates a virtualenv environment based on the system Python in the project folder.

If you do not have the Python version in your system, you can download and install it.

![Downloading and installing Python](https://resources.jetbrains.com/help/img/idea/2025.3/py_download_python.png)

This feature is available only on Windows and macOS.

uv
    

IntelliJ IDEA configures a uv environment as the project interpreter.

Base conda
    

IntelliJ IDEA configures a conda base environment as the project interpreter.

To configure an interpreter of another type or to use an existing environment, select Custom environment.

The following steps depend on your choice:

![Create a project with virtualenv](https://resources.jetbrains.com/help/img/idea/2025.3/ij_new_project_virtualenv.png)
     * Select Virtualenv from the list of environment types.

     * Select the base interpreter from the list, or click ![Choose the base interpreter](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) and find the Python executable in your file system.

If you do not have the Python version in your system, you can download and install it.

![Downloading and installing Python](https://resources.jetbrains.com/help/img/idea/2025.3/py_download_python.png)

This feature is available only on Windows and macOS.

     * Specify the location of the new virtual environment in the Location field, or click ![Virtual environment location](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) and browse for the location in your file system. The directory for the new virtual environment should be empty.

     * Select the Inherit packages from base interpreter checkbox if you want all packages installed in the global Python on your machine to be added to the virtual environment you're going to create. This checkbox corresponds to the `--system-site-packages` option of the [virtualenv](http://www.virtualenv.org/en/latest/index.html) tool.

     * Select the Make available to all projects checkbox if you want to reuse this environment when creating Python interpreters in IntelliJ IDEA.

![Create a project with a conda environment](https://resources.jetbrains.com/help/img/idea/2025.3/ij_new_project_conda.png)
     * Select Conda from the list of environment types.

     * Select the Python version from the list.

     * Specify the environment name.

     * IntelliJ IDEA will detect a conda installation.

If IntelliJ IDEA did not detect the installation automatically, specify the location of the conda executable, or click ![Conda executable location](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) to browse for it.

![Create a project with Pipenv](https://resources.jetbrains.com/help/img/idea/2025.3/ij_new_project_pipenv.png)
     * Select Pipenv from the list of environment types.

     * Select the base interpreter from the list, or click ![Browse...](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) and find the Python executable in your file system.

If you do not have the Python version in your system, you can download and install it.

![Downloading and installing Python](https://resources.jetbrains.com/help/img/idea/2025.3/py_download_python.png)

This feature is available only on Windows and macOS.

     * If you have added the base binary directory to your `PATH` environmental variable, you do not need to set any additional options: the path to the pipenv executable will be autodetected.

If IntelliJ IDEA does not detect the pipenv executable, click Install pipenv via pip to allow IntelliJ IDEA to install it for you automatically.

Alternatively, follow the pipenv installation procedure to discover the executable path and then specify it in the dialog.

![Create a project with Poetry](https://resources.jetbrains.com/help/img/idea/2025.3/ij_new_project_poetry.png)
     * Select Poetry from the list of environment types.

     * Select the base interpreter from the list or click ![Browse...](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) and find the Python executable in your file system.

If you do not have the Python version in your system, you can download and install it.

![Downloading and installing Python](https://resources.jetbrains.com/help/img/idea/2025.3/py_download_python.png)

This feature is available only on Windows and macOS.

     * If IntelliJ IDEA does not detect the Poetry installation, click Install poetry via pip to allow IntelliJ IDEA to install Poetry for you automatically.

Alternatively, specify the location of the Poetry executable, or click ![Browse...](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) to browse for it.

     * To create a virtual environment within the project directory, select the Create an in-project environment checkbox.

![Create a project with uv](https://resources.jetbrains.com/help/img/idea/2025.3/ij_new_project_uv.png)
     * Select uv from the list of environment types.

     * Select the base interpreter from the list, or click ![Choose the base interpreter](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) and find the Python executable in your file system.

     * IntelliJ IDEA will detect a uv installation.

Otherwise, specify the location of the uv executable, or click ![uv executable location](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) to browse for it.

![Create a project with Hatch](https://resources.jetbrains.com/help/img/idea/2025.3/ij_new_project_hatch.png)
     * Select Hatch from the list of environment types.

     * IntelliJ IDEA will detect a Hatch installation.

Otherwise, specify the location of the Hatch executable, or click ![uv executable location](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) to browse for it.

     * Select an environment.

Hatch environments are workspaces designed for various project-specific tasks. If no environment is explicitly selected, Hatch will use the [default environment](https://hatch.pypa.io/latest/tutorials/environment/basic-usage/).

     * Select the base interpreter from the list, or click ![Choose the base interpreter](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) and find the Python executable in your file system.

If you do not have the Python version in your system, you can download and install it.

![Downloading and installing Python](https://resources.jetbrains.com/help/img/idea/2025.3/py_download_python.png)

This feature is available only on Windows and macOS.

![Selecting an existing conda interpreter for a new project](https://resources.jetbrains.com/help/img/idea/2025.3/ij_new_project_existing_conda.png)

To reuse an existing conda environment:

     * Switch Type to Conda.

     * Specify the environment name.

     * IntelliJ IDEA will detect a conda installation.

If IntelliJ IDEA did not detect the installation automatically, specify the location of the conda executable, or click ![Conda executable location](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) to browse for it.

     * Select the environment from the list. If you specified the path to conda manually, you may need to reload environments.

![Selecting an existing interpreter for a new project](https://resources.jetbrains.com/help/img/idea/2025.3/ij_new_project_existing_other.png)

To reuse a different Python environment:

     * Switch Type to Python.

     * Select the Python executable from the list or click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) to browse for it.

  4. Click Create.




15 July 2025

[Configure a Python SDK](configuring-python-sdk.html)[Python Code Running Assistance](code-running-assistance-tutorial.html)
