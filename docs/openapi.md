[//]: # (Source: https://www.jetbrains.com/help/idea/openapi.html)
[//]: # (Downloaded: 2025-12-17 19:33:30)

## Create an OpenAPI specification

IntelliJ IDEA recognizes a dedicated OpenAPI Specification file type with relevant [coding assistance](discover-intellij-idea.html#coding-assistance). These are regular YAML or JSON files with the definition of the OpenAPI specification version.

### Create an OpenAPI Specification manually

  1. In the Project tool window, press `Alt+Insert` and select OpenAPI Specification from the context menu.

  2. Specify a name for the file and select the specification version and file format.

![New OpenAPI specification](https://resources.jetbrains.com/help/img/idea/2025.3/openapi_create_new_specification.png)



In an OpenAPI specification opened in the editor, use the ![Add icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg) gutter icons to quickly add specification sections.

![OpenAPI gutter icons](https://resources.jetbrains.com/help/img/idea/2025.3/openapi_gutter_icons_add.png)

You can disable the ![Add icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg) gutter icon in the IDE settings, under Languages & Frameworks | OpenAPI Specifications using the Gutter icons for quick specification edits checkbox.

Depending on the format and version, the new OpenAPI specification file contains the following template:

openapi: 3.0.0 info: title: Title description: Title version: 1.0.0 servers: \- url: 'https' paths: 

{ "openapi": "3.0.0", "info": { "title": "Title", "description": "Title", "version": "1.0.0" }, "servers": [ { "url": "https" } ], "paths": { } } 

swagger: "2.0" info: title: Title description: Title version: 1.0.0 host: www schemes: \- https paths: 

{ "swagger": "2.0", "info": { "title": "Title", "description": "Title", "version": "1.0.0" }, "host": "www", "schemes": [ "https" ], "paths": { } } 

If you start with an empty YAML or JSON file, you can type `opnp` or `swag` and press `Tab` to insert the corresponding [live template](using-live-templates.html).

### Generate an OpenAPI Specification based on URL mapping

If you have a REST controller with URL mapping in your source code, you can quickly generate an OpenAPI Specification from the controller code.

  1. Click ![Show available actions for URL](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.inlayGlobe.svg) next to a controller path.

  2. Select Generate OpenAPI draft.


![Generate OpenAPI action](https://resources.jetbrains.com/help/img/idea/2025.3/openapi_generate_action.png)

The generated file is saved under Scratches and Consoles | OpenAPI Specifications.

The action is also available in the Endpoints tool window where you can also generate an OpenAPI specification for the entire module.

### Reference a definition from a separate file

With OpenAPI 3.0, you can reference a definition hosted on any location using the [$ref](https://swagger.io/docs/specification/using-ref/) keyword. IntelliJ IDEA provides you with path completion, validation, and quick navigation. For completion, IntelliJ IDEA understands the context of the current file and of external files, and suggests using pointers to relevant elements.

  1. Enter the `$ref` keyword.

  2. Start typing the path to the external definition.




You can press `Ctrl+B` to quickly navigate to the file and element you refer to.

![OpenAPI use ref](https://resources.jetbrains.com/help/img/idea/2025.3/openapi_ref.png)
