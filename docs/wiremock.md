[//]: # (Source: https://www.jetbrains.com/help/idea/wiremock.html)
[//]: # (Downloaded: 2025-12-17 20:06:59)

## Create WireMock stubs

### Create basic WireMock stub from scratch

If a JSON file is placed in the mappings folder or contains the `"mappings"` key, IntelliJ IDEA recognizes it as a WireMock stub file and provides appropriate coding assistance.

  1. In the Project tool window, right-click a folder (or press `Alt+Insert`) and select New | File.

  2. In the New File dialog that opens, enter a name of the file. For example, you can enter `mappings/my-stub.json`, and IntelliJ IDEA will create the mappings folder and place the new file within it.

  3. Start typing a key to get suggestions for applicable keys and their quick documentation.


![Wiremock Coding Assistance](https://resources.jetbrains.com/help/img/idea/2025.3/wiremock_coding_assistance.png)

### Create WireMock stubs from Endpoints tool window

  1. Open the Endpoints tool window (View | Tool Windows | Endpoints).

  2. Right-click an endpoint and select Generate WireMock Stubs.


![Creating WireMock stub from Endpoints](https://resources.jetbrains.com/help/img/idea/2025.3/wiremock_stub_from_endpoints.png)

The new stub file is saved as a [scratch](scratches.html) under Scratches and Consoles | WireMock Stubs.

### Create WireMock stubs from OpenAPI specification

  1. Open an OpenAPI specification file.

  2. Click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.gutter.run.svg) and select Generate WireMock Stubs.


![Creating WireMock stub from Endpoints](https://resources.jetbrains.com/help/img/idea/2025.3/wiremock_stub_from_openapi_specification.png)

The new stub file is saved as a [scratch](scratches.html) under Scratches and Consoles | WireMock Stubs.
