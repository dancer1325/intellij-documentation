[//]: # (Source: https://www.jetbrains.com/help/idea/configuring-goroot-and-gopath.html)
[//]: # (Downloaded: 2025-12-17 19:21:46)

## GOROOT

The GOROOT setting defines which Go SDK version IntelliJ IDEA uses for your project. You can either download a new version directly from the IDE or configure a local installation.

### Configure GOROOT

  * Open settings (`Ctrl+Alt+S`) and navigate to Languages & Frameworks | Go GOROOT.

Select a Go version from the list. If none is available, click Add SDK to either [download a Go version](#download-go-sdk) or [select a local Go SDK installation](#navigate-to-go-sdk).




### Select a local Go SDK

Ensure the selected folder includes both bin and src directories.

  1. Open settings (`Ctrl+Alt+S`) and go to Languages & Frameworks | Go GOROOT.

  2. Click the Add SDK button (![the Add SDK button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)), then select Local.

  3. In the file browser, navigate to the Go SDK folder on your system.

  4. Click Open to confirm.

![Select a local copy of Go SDK](https://resources.jetbrains.com/help/img/idea/2025.3/go_ij_select_go_version.png)



### Download the Go SDK

  1. Open settings (`Ctrl+Alt+S`) and navigate to Languages & Frameworks | Go GOROOT.

  2. Click the Add SDK button (![the Add SDK icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)) and select Download.

  3. From the list, select the desired Go SDK version.

  4. In the Location field, specify where to install the SDK. To browse for a location, click the Browse icon (![the Browse icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.menu-open_dark.svg)).

  5. Click OK to confirm the download and installation settings.

When you click Apply or OK in the settings dialog, IntelliJ IDEA downloads and unpacks the selected Go SDK automatically.

![Download the Go SDK](https://resources.jetbrains.com/help/img/idea/2025.3/go_ij_download_go_sdk_settings.png)



### Using asdf

You can use asdf to manage multiple Go versions for your projects. IntelliJ IDEA recognizes Go SDKs installed and managed through asdf, allowing you to switch between them directly in the IDE.

To use asdf as a Go SDK management tool, make sure you have installed [asdf](https://asdf-vm.com/guide/getting-started.html#_3-install-asdf) and the required Go versions via the [asdf installation guide](https://asdf-vm.com/guide/getting-started.html#_5-install-a-version).

asdf is a version manager that handles multiple programming languages and utilities. It lets you define different Go versions globally or per project directory:

  * `asdf global`: sets the default Go version for the entire system.

  * `asdf local`: sets the Go version for a specific project or directory.




IntelliJ IDEA supports both `asdf local` and `asdf global` configurations. You can also specify multiple versions, for example: `asdf local golang 1.21.0 1.20.8`. The IDE automatically detects the configured versions and displays them in the Go SDK list.

### Select an asdf-managed Go version for the project

  1. Open settings (`Ctrl+Alt+S`) and navigate to Go | GOROOT.

  2. From the list of available SDKs, select the Go version managed by asdf. If asdf is installed and configured, the versions it provides will appear automatically.




Once the version is selected, IntelliJ IDEA uses the corresponding Go SDK for building, running, and testing your project. You can change the version at any time using the same settings page or by updating your `.tool-versions` file in the project directory.
