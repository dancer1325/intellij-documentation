[//]: # (Source: https://www.jetbrains.com/help/idea/prerequisites-for-dev-containers.html)
[//]: # (Downloaded: 2025-12-17 19:34:11)

## Prerequisites for a local Dev Container

  * You have a project that contains the `.devcontainer` folder with the [`devcontainer.json`](https://containers.dev/implementors/json_reference/) file that describes the actual Dev Container.

Currently, the code completion for the `devcontainer.json` file is limited. However, the following properties are available:

    * [Build properties](https://containers.dev/implementors/json_reference/#image-specific) are supported.

    * [General properties](https://containers.dev/implementors/json_reference/#general-properties).

    * [Docker compose properties](https://containers.dev/implementors/json_reference/#compose-specific) are supported.

    * [Lifecycle scripts](https://containers.dev/implementors/json_reference/#lifecycle-scripts) are supported.

    * In [port attributes](https://containers.dev/implementors/json_reference/#port-attributes) only `label` is supported.

    * The [minimal host requirements](https://containers.dev/implementors/json_reference/#min-host-reqs) are not supported.

    * [Variables in `devcontainer.json`](https://containers.dev/implementors/json_reference/#variables-in-devcontainerjson) are supported.

  * You have access to GitHub.

  * You have the Git 2.20.1 version or later installed on your machine.

  * You have a [running SSH agent](using-ssh-keys.html) on your local machine. 

For example, on Windows, when you build a Dev Container from the GitHub repository using the SSH URL, the `- git clone` operation (cloning the repository sources to the Docker volume connected to the auxiliary container) cannot be performed without the running SSH agent.

  * You have [Docker](https://docs.docker.com/get-docker/) installed on the machine where a Dev Container will reside.

  * The minimal backend requirement for mounting sources is the installed Docker. Docker alternatives, such as [Colima](https://github.com/abiosoft/colima), or similar are not yet supported. [Podman](https://github.com/containers/podman-compose) support is under development. 

If you encounter issues working with these Docker alternatives, submit a bug report to the issue tracker.

  * Your Docker resources meet the [minimal system requirements](prerequisites.html) for the backend.



