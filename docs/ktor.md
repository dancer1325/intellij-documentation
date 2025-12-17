[//]: # (Source: https://www.jetbrains.com/help/idea/ktor.html)
[//]: # (Downloaded: 2025-12-17 19:31:00)

## Create a new Ktor project

  1. On the Welcome screen, click New Project.

Otherwise, go to File | New | Project in the main menu.

  2. In the New Project wizard, choose Ktor from the list on the left.

  3. On the right pane, you can specify the following settings:

![Ktor Project Settings](https://resources.jetbrains.com/help/img/idea/2025.3/ktor_idea_new_project_settings.png)
     * Name: Specify a project name.

     * Location: Specify a directory for your project.

     * Build System: Choose the desired [build system](https://ktor.io/docs/server-dependencies.html). This can be Gradle with Kotlin or Groovy DSL, or Maven.

     * Website: Specify a domain used to generate a package name.

     * Artifact: This field shows a generated artifact name.

     * Ktor version: Choose the required Ktor version.

     * Engine: Select an [engine](https://ktor.io/docs/engines.html) used to run a server.

     * Configuration in: Choose whether to specify server parameters [in code, in a HOCON or Yaml file](https://ktor.io/docs/create-server.html).

     * Add sample code: Use this option to add sample code for plugins, which will be added on the next page.

You can also generate a plugin's code for the existing project using the [completion popup](#generate-plugin-code).

  4. On the next page, you can choose a set of [plugins](https://ktor.io/docs/plugins.html) \- building blocks that provide common functionality of a Ktor application, such as authentication, serialization and content encoding, compression, cookie support, and so on.

![Ktor plugins](https://resources.jetbrains.com/help/img/idea/2025.3/ktor_idea_new_project_plugins_list.png)

Click Create and wait until IntelliJ IDEA generates a project and installs the dependencies.



