[//]: # (Source: https://www.jetbrains.com/help/idea/go-gopath.html)
[//]: # (Downloaded: 2025-12-17 19:28:13)

## Create a GOPATH project

By default, IntelliJ IDEA creates a project with Go modules integration. You can disable this option in settings. But ensure that you keep the necessary file structure and store your project under GOPATH. For more information about storing your code under GOPATH, refer to [How to Write Go Code (with GOPATH) at go.dev](https://go.dev/doc/gopath_code).

Firstly, you need to create a default Go project with Go modules integrations but be sure to place your project under GOPATH.

### Create a Go project

  1. Select File | New | New Project. 

Alternatively, navigate to New | Project on the Welcome to IntelliJ IDEA dialog.

  2. In the New Project dialog, select New Project from the list of available project types.

Ensure that Go is selected as the project language in the Language list.

  3. In the GOROOT field, specify the location of your Go installation. IntelliJ IDEA usually detects this location automatically.

To change or install a new Go SDK version, click Add SDK (![Add SDK icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg)) and choose one of the following options:

     * Local: to use an existing SDK from your local system.

     * Download: to download a Go SDK version from the official repository.

  4. (Optional) Select or clear the Enable vendoring support automatically checkbox to enable or disable vendoring support.

  5. (Optional) In the Environment field, specify any environment variables your project requires. For example, `GOPROXY`.

To learn more, refer to the [Environment variables section](create-a-project-with-go-modules-integration.html#environment-variables).

Do not use this field to set tags for the `GOEXPERIMENT` variable. Instead, use the Experiments field in the Build Tags settings. For details, see [Using Go experiments](configuring-build-constraints-and-vendoring.html#using_go_experiments).

  6. Click Create to create the project.

![Download Go SDK](https://resources.jetbrains.com/help/img/idea/2025.3/go_ij_create_go_modules_project.png)



Secondly, disable Go modules integration.

### Disable the Go modules integration

  1. Press `Ctrl+Alt+S` to open settings and then select Languages & Frameworks | Go Go Modules.

  2. Clear the Enable Go modules integration checkbox.

![Enable Go modules integration](https://resources.jetbrains.com/help/img/idea/2025.3/go_enable_go_modules_integration.png)


