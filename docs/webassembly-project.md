[//]: # (Source: https://www.jetbrains.com/help/idea/webassembly-project.html)
[//]: # (Downloaded: 2025-12-17 20:06:58)

# WebAssembly (Wasm)

WebAssembly (Wasm) is a binary format that you can run in a browser. IntelliJ IDEA supports generating WASM files from GO source files. To learn more, refer to the [official WebAssembly documentation](https://webassembly.org/).

### Create a Go project

  1. Select File | New | New Project. 

Alternatively, navigate to New | Project on the Welcome to IntelliJ IDEA dialog.

  2. In the New Project dialog, select Go from the list of available project types.

Ensure that Go is selected as the project language in the Language list.

  3. In the GOROOT field, specify the location of your Go installation. IntelliJ IDEA usually detects this location automatically.

To change or install a new Go SDK version, click Add SDK (![Add SDK icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg)) and choose one of the following options:

     * Local: to use an existing SDK from your local system.

     * Download: to download a Go SDK version from the official repository.




### Configure the project for generating WASM files

  1. Open settings `Ctrl+Alt+S`, and navigate to Languages & Frameworks | Go | Build Tags.

  2. From the OS list, select js.

  3. From the Arch list, select wasm.

  4. Click OK.

  5. On the main toolbar, click Run | Edit Configurations.

  6. Click the Add New Configuration icon (![The Add New Configuration icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)) or press `Alt+Insert`.

  7. From the Run kind list, select File.

  8. In the Files field, add the name of the GO file you want to run (for example, `main.go`).

  9. Clear the Run after build checkbox.

  10. In the Environment field, click the Browse button at the end of the field.

In the Environment Variables dialog, add the following environment variables:

     * `GOOS=js`

     * `GOARCH=wasm`

  11. In the Go tool arguments field, replace the `-i` argument with `-o main.wasm`, where `main.wasm` is the name of the output WASM file.

  12. Click OK.

  13. Click the Run <configuration_name> icon or press `Shift+F10`.

As a result, a new WASM file appears in the Project tool window.




To add an environment variable, click the Add icon. Enter the variable name in the Name column and its value in the Value column.

24 June 2025

[Go (GOPATH)](go-gopath.html)[Go configuration](go-configuration.html)
