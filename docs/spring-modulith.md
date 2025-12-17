[//]: # (Source: https://www.jetbrains.com/help/idea/spring-modulith.html)
[//]: # (Downloaded: 2025-12-17 20:03:06)

## Structure of a modular application

A Spring Modulith application usually consists of:

  * A main package with a class that is used to run the application. This class is annotated with `@SpringBootApplication` and usually has the `main(…)` method used to run it.

  * Application modules — direct sub-packages of the main package that have:

    * Provided interface: an API made available to other modules, typically implemented using Spring beans and domain events published by the module.

    * Internal implementation components: intended for internal use within the module, not accessible from outside.

    * Required interface: a module's use of other modules' features, like calling their Spring beans, listening to their events, or using their exposed configuration properties.




Here is an example arrangement of a simple application:

Demo ╰─ src/main/java ╰─ bookstore // main package ╰─ BookstoreMainApplication.java ╰─ catalog // application module package ╰─ ProductApi.java // provided interface ╰─ domain ╰─ ProductService.java // internal component ╰─ common ╰─ orders ╰─ web ╰─ OrderRestController.java // ProductApi is required interface ╰─ config 

`OrderRestController.java` from the `orders` module here has a dependency on the exposed `ProductApi.java` from the `catalog` module.

Check the official [Spring Modulith documentation](https://docs.spring.io/spring-modulith/reference/index.html) for more details.

In IntelliJ IDEA, as soon as you open the Project tool window `Alt+1`, you can review the structure of your modular application and navigate between its parts.

In the picture below, there is a modular application with top-level modules marked by a green lock and internal components marked by a red lock.

![Project with open and closed modules](https://resources.jetbrains.com/help/img/idea/2025.3/open_and_closed_modules.png)

Also, you can inspect the [logical structure](viewing-structure-of-a-source-file.html#logical-structure) of the application from the framework's point of view: select the main application class that is annotated with `@SpringBootApplication` and press `Alt+7` (or go to View | Tool Windows | Structure in the main menu).

[![List of the application's modules in the Structure tool window](https://resources.jetbrains.com/help/img/idea/2025.3/modular_application_structure.png)](https://resources.jetbrains.com/help/img/idea/2025.3/modular_application_structure.png)

The Modulith-specific ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.objectBrowser.flattenModules.svg) Modules node shows the list of application's modules, their IDs, allowed dependencies, and named interfaces.
