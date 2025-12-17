[//]: # (Source: https://www.jetbrains.com/help/idea/spring-file-templates.html)
[//]: # (Downloaded: 2025-12-17 20:03:03)

# Spring file templates

[File templates](using-file-and-code-templates.html) are reusable blueprints that define the default structure and initial content for files you create in your project. For Spring, IntelliJ IDEA provides file templates for component files and XML configuration files.

### Use Spring component file templates

  1. Right-click a directory under main/java or main/kotlin and select New (or press `Alt+Insert`).

To use the Spring Boot Test template, right-click your test directory or another [Test Sources Root](testing.html#add-test-root) directory.

  2. Select Spring Java Component (for Java projects) or Spring Kotlin Component (for Kotlin projects).

  3. Select a type of the component, such as a Controller for a `@RestController` class or Application for a `@SpringBootApplication` class.

Controller, RestController, and Controller Advice templates are available if the project has the `spring-web` dependency. The Repository template is available if the project has the `spring-data-commons` dependency.

![Spring file templates](https://resources.jetbrains.com/help/img/idea/2025.3/spring_file_templates.png)



The created file will include the package name and all the necessary imports and annotations.

Spring component file templates are also available in the [Generate](generating-code.html) action. With your class source code opened in the editor, press `Alt+Insert` and select Spring Component.

![Spring file templates](https://resources.jetbrains.com/help/img/idea/2025.3/spring_generate_new_component.png)

### Use Spring XML configuration file templates

  1. Right-click the resources directory and select New (or press `Alt+Insert`).

  2. Select XML Configuration File | Spring Config.

  3. Enter a name for your configuration file.




In projects prior to Spring 2.0, this will create DTD-based XML files. In Spring 2.0 and later, this will create Schema (XSD)-based XML files.

### Customize Spring file templates

  1. In the Settings dialog (`Ctrl+Alt+S`) , go to Editor | File and Code Templates.

  2. Open the Other tab, expand the Spring category, and customize the templates.

![Spring file templates](https://resources.jetbrains.com/help/img/idea/2025.3/settings_spring_file_templates.png)



By default, file templates are created at the IDE level: template modifications are available in all projects that you open with the current IDE instance. For more information about template scopes and sharing templates, refer to [Share file templates](share-file-templates.html).

17 February 2025

[Spring tool window](spring-tool-window.html)[Scheduled Tasks](scheduled-tasks.html)
