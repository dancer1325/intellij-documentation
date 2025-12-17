[//]: # (Source: https://www.jetbrains.com/help/idea/configuring-python-sdk.html)
[//]: # (Downloaded: 2025-12-17 19:21:59)

## Configure local Python interpreters

To configure a local Python interpreter, adhere to one of the following procedures:

### Create a virtualenv environment

  1. Navigate to File | Project Structure or press `Ctrl+Alt+Shift+S`.

  2. In the Project Structure dialog, select SDKs under the Platform Settings section, click ![Add a new SDK](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg), and choose Add Python SDK from disk... from the popup menu. 

![Adding a new Python SDK](https://resources.jetbrains.com/help/img/idea/2025.3/ij_add_Python_sdk.png)
  3. The following actions depend on whether you want to generate a new virtual environment or to use an existing one.

New virtualenv environment
    ![Generate new virtualenv environment](https://resources.jetbrains.com/help/img/idea/2025.3/ij_new_virtualenv_environment.png)
     1. Select Virtualenv from the list of environment types.

     2. Select the base interpreter from the list, or click ![Choose the base interpreter](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) and find the Python executable in your file system.

     3. Specify the location of the new virtual environment in the Location field, or click ![Virtual environment location](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) and browse for the location in your file system. The directory for the new virtual environment should be empty.

     4. Select the Inherit packages from base interpreter checkbox if you want all packages installed in the global Python on your machine to be added to the virtual environment you're going to create. This checkbox corresponds to the `--system-site-packages` option of the [virtualenv](http://www.virtualenv.org/en/latest/index.html) tool.

     5. Select the Make available to all projects checkbox if you want to reuse this environment when creating Python interpreters in IntelliJ IDEA.

Existing virtualenv environment
    ![Select existing virtualenv environment](https://resources.jetbrains.com/help/img/idea/2025.3/ij_existing_virtualenv_environment.png)
     * Select Python from the list of environment types.

     * Select the required interpreter from the list.

If the required interpreter is not on the list, click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg), and then browse for the required Python executable (for example, venv/bin/python on macOS or venv\Scripts\python.exe on Windows).

The selected virtual environment will be reused for the current project.

  4. Click OK to complete the task.




If IntelliJ IDEA displays the Invalid environment warning, it means that the specified Python binary cannot be found in the file system, or the Python version is [not supported](python.html#support). Check the Python path and [install a new version](https://www.python.org/downloads/), if needed.

For more information, refer to the [PyCharm documentation](https://www.jetbrains.com/help/pycharm/creating-virtual-environment.html).

### Create a conda environment

  1. Ensure that [Anaconda](https://www.continuum.io/) or [Miniconda](https://conda.io/en/latest/miniconda.html) is downloaded and installed on your computer, and you are aware of a path to its executable file.

For more information, refer to the [installation instructions](https://docs.anaconda.com/anaconda/install/).

  2. Navigate to File | Project Structure or press `Ctrl+Alt+Shift+S`.

  3. In the Project Structure dialog, select SDKs under the Platform Settings section, click ![Add a new SDK](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg), and choose Add Python SDK from disk... from the popup menu. 

![Adding a new Python SDK](https://resources.jetbrains.com/help/img/idea/2025.3/ij_add_Python_sdk.png)
  4. The following actions depend on whether you want to create a new conda environment or to use an existing one. 

New conda environment
    ![Generate new conda environment](https://resources.jetbrains.com/help/img/idea/2025.3/ij_new_conda_environment.png)
     1. Select Conda from the list of environment types.

     2. Select the Python version from the list.

     3. Specify the environment name.

     4. IntelliJ IDEA will detect a conda installation.

If IntelliJ IDEA did not detect the installation automatically, specify the location of the conda executable, or click ![Conda executable location](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) to browse for it.

Existing conda environment
    ![Select existing conda environment](https://resources.jetbrains.com/help/img/idea/2025.3/ij_existing_conda_environment.png)
     1. Select Conda from the list of environment types.

     2. IntelliJ IDEA will detect a conda installation.

If IntelliJ IDEA did not detect the installation automatically, specify the location of the conda executable, or click ![Browse...](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) to browse for it.

     3. Select the environment from the list.

The selected conda environment will be reused for the current project.

  5. Click OK to complete the task.




For more information, refer to the [PyCharm documentation](https://www.jetbrains.com/help/pycharm/conda-support-creating-conda-virtual-environment.html).

### Create a pipenv environment

  1. Navigate to File | Project Structure or press `Ctrl+Alt+Shift+S`.

  2. In the Project Structure dialog, select SDKs under the Platform Settings section, click ![Add a new SDK](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg), and choose Add Python SDK from disk... from the popup menu. 

![Adding a new Python SDK](https://resources.jetbrains.com/help/img/idea/2025.3/ij_add_Python_sdk.png)
  3. Select Pipenv from the list of environment types. 

![Generate new pipenv environment](https://resources.jetbrains.com/help/img/idea/2025.3/ij_new_pipenv_environment.png)
  4. Select the base interpreter from the list, or click ![Browse...](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) and find the Python executable in your file system.

  5. If you have added the base binary directory to your `PATH` environmental variable, you do not need to set any additional options: the path to the pipenv executable will be autodetected.

If IntelliJ IDEA does not detect the pipenv executable, click Install pipenv via pip to allow IntelliJ IDEA to install it for you automatically.

Alternatively, follow the pipenv installation procedure to discover the executable path and then specify it in the dialog.

  6. Click OK to complete the task.




If IntelliJ IDEA displays the Invalid environment warning, it means that the specified Python binary cannot be found in the file system, or the Python version is [not supported](python.html#support). Check the Python path and [install a new version](https://www.python.org/downloads/), if needed.

When you have set the pipenv virtual environment as a Python interpreter, all available packages are added from the source defined in Pipfile. The packages are installed, removed, and updated in the list of the packages through pipenv rather than through pip.

For more information, refer to the [PyCharm documentation](https://www.jetbrains.com/help/pycharm/pipenv.html).

### Create a Poetry environment

  1. Navigate to File | Project Structure or press `Ctrl+Alt+Shift+S`.

  2. In the Project Structure dialog, select SDKs under the Platform Settings section, click ![Add a new SDK](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg), and choose Add Python SDK from disk... from the popup menu. 

![Adding a new Python SDK](https://resources.jetbrains.com/help/img/idea/2025.3/ij_add_Python_sdk.png)
  3. The following actions depend on whether you want to create a new Poetry environment or to use an existing one.

New Poetry environment
    ![Generate new poetry environment](https://resources.jetbrains.com/help/img/idea/2025.3/ij_new_poetry_environment.png)
     1. Select Poetry from the list of environment types.

     2. Select the base interpreter from the list or click ![Browse...](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) and find the Python executable in your file system.

     3. IntelliJ IDEA will detect a Poetry installation.

If IntelliJ IDEA does not detect the Poetry installation, click Install poetry via pip to allow IntelliJ IDEA to install Poetry for you automatically.

Alternatively, specify the location of the Poetry executable, or click ![Browse...](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) to browse for it.

     4. To create a virtual environment within the project directory, select the Create an in-project environment checkbox.

Existing Poetry environment
    ![Select existing poetry environment](https://resources.jetbrains.com/help/img/idea/2025.3/ij_existing_poetry_environment.png)
     1. Select Poetry from the list of environment types.

     2. IntelliJ IDEA will detect a Poetry installation.

If IntelliJ IDEA did not detect the installation automatically, specify the location of the executable, or click ![Browse...](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) to browse for it.

     3. Select the environment from the list.

The selected Poetry environment will be reused for the current project.

  4. Click OK to complete the task.




For more information, refer to the [PyCharm documentation](https://www.jetbrains.com/help/pycharm/poetry.html).

### Create a uv environment

  1. Navigate to File | Project Structure or press `Ctrl+Alt+Shift+S`.

  2. In the Project Structure dialog, select SDKs under the Platform Settings section, click ![Add a new SDK](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg), and choose Add Python SDK from disk... from the popup menu. 

![Adding a new Python SDK](https://resources.jetbrains.com/help/img/idea/2025.3/ij_add_Python_sdk.png)
  3. The following actions depend on whether you want to generate a new virtual environment or to use an existing one.

New uv environment
    ![Generate new uv environment](https://resources.jetbrains.com/help/img/idea/2025.3/ij_new_uv_environment.png)
     1. Select uv from the list of environment types.

     2. Select the base interpreter from the list, or click ![Choose the base interpreter](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) and find the Python executable in your file system.

     3. IntelliJ IDEA will detect a uv installation.

If IntelliJ IDEA did not detect the installation automatically, specify the location of the uv executable, or click ![Browse...](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) to browse for it.

Existing uv environment
    ![Select existing uv environment](https://resources.jetbrains.com/help/img/idea/2025.3/ij_existing_uv_environment.png)
     1. Select uv from the list of environment types.

     2. IntelliJ IDEA will detect a uv installation.

If IntelliJ IDEA did not detect the installation automatically, specify the location of the uv executable, or click ![Browse...](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) to browse for it.

     3. Select the environment from the list.

The selected uv environment will be reused for the current project.

  4. Click OK to complete the task.




For more information, refer to the [PyCharm documentation](https://www.jetbrains.com/help/pycharm/uv.html).

### Create a Hatch environment

  1. Navigate to File | Project Structure or press `Ctrl+Alt+Shift+S`.

  2. In the Project Structure dialog, select SDKs under the Platform Settings section, click ![Add a new SDK](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg), and choose Add Python SDK from disk... from the popup menu. 

![Adding a new Python SDK](https://resources.jetbrains.com/help/img/idea/2025.3/ij_add_Python_sdk.png)
  3. The following actions depend on whether you want to generate a new virtual environment or to use an existing one.

New Hatch environment
    ![Generate new Hatch environment](https://resources.jetbrains.com/help/img/idea/2025.3/ij_new_hatch_environment.png)
     1. Select Hatch from the list of environment types.

     2. IntelliJ IDEA will detect a Hatch installation.

If IntelliJ IDEA did not detect the installation automatically, specify the location of the Hatch executable, or click ![Browse...](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) to browse for it.

     3. Select an environment.

Hatch environments are workspaces designed for various project-specific tasks. If no environment is explicitly selected, Hatch will use the [default environment](https://hatch.pypa.io/latest/tutorials/environment/basic-usage/).

     4. Select the base interpreter from the list, or click ![Choose the base interpreter](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) and find the Python executable in your file system.

Existing Hatch environment
    ![Select existing Hatch environment](https://resources.jetbrains.com/help/img/idea/2025.3/ij_existing_hatch_environment.png)
     1. Select Hatch from the list of environment types.

     2. IntelliJ IDEA will detect a Hatch installation.

If IntelliJ IDEA did not detect the installation automatically, specify the location of the Hatch executable, or click ![Browse...](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) to browse for it.

     3. Select the environment from the list.

  4. Click OK to complete the task.




For more information, refer to the [PyCharm documentation](https://www.jetbrains.com/help/pycharm/hatch.html).
