[//]: # (Source: https://www.jetbrains.com/help/idea/spring-boot.html)
[//]: # (Downloaded: 2025-12-17 20:02:59)

## Custom configuration files

Spring Initializr creates one default configuration file that may not always be sufficient for development. If you do not want to use the default configuration file, or if you want to run your code in different environments, you can use custom configuration files defined in your project.

Let IntelliJ IDEA know which files are configuration files in your project to enable relevant highlighting and coding assistance:

### Define project configuration files

  1. In the main menu, go to File | Project Structure or press `Ctrl+Alt+Shift+S` to open the Project Structure dialog.

  2. Add the Spring facet: from the left-hand list, select Facets, click ![the Add icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg), and select Spring.

  3. In the right-hand section, select Configuration Files and click ![Customize Spring Boot](https://resources.jetbrains.com/help/img/idea/2025.3/spring-boot-core.icons.expui.springBoot.svg) (Customize Spring Boot) in the toolbar.

  4. If you want to use a custom configuration file instead of the default one, type its name in the `spring.config.name` field.

If you want to use multiple configuration files, click ![The Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select files from the project tree.

Valid configuration files are marked with ![The Spring Boot icon](https://resources.jetbrains.com/help/img/idea/2025.3/spring-boot-core.icons.expui.springBoot.svg).

  5. Click OK and apply the changes.


![Configuring a custom configuration file](https://resources.jetbrains.com/help/img/idea/2025.3/spring_boot_custom_config.png)

Some custom configuration files are detected automatically. For example, profile-specific configuration files with names that match the current naming pattern will be added to the context.
