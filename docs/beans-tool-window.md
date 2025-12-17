[//]: # (Source: https://www.jetbrains.com/help/idea/beans-tool-window.html)
[//]: # (Downloaded: 2025-12-17 19:18:43)

# Beans tool window

The Beans tool window provides a view of Spring, Micronaut, and Java Contexts and Dependency Injection (CDI) beans detected in your project.

If only one of these technologies is used in your project, the tool window will have the corresponding name: Spring, Micronaut, or CDI. If multiple frameworks are used, the tool window will have the Beans name with the option to filter beans by framework.

![Beans tool window](https://resources.jetbrains.com/help/img/idea/2025.3/beans_tool_window.png)

IntelliJ IDEA provides extensive support for Spring beans. When you select a Spring bean in this tool window, you can view graphs of bean dependencies, controller mappings, and JPA queries. For more information, refer to [Spring tool window](spring-tool-window.html).

### Filter beans

Use the following tools to filter beans in the tool window:

  * Click Module to show only beans from a particular module. To show beans from multiple modules, click Select.

  * Click Type to filter Spring or Micronaut beans by type. To show multiple types of beans, click Select.

  * Click ![Options](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.show.svg) to group beans by module or to show additional beans:

    * Show From Libraries: Include beans defined in libraries (shown in yellow).

    * Show From Tests: Include beans defined in tests (shown in green).

    * Show Implicit Beans: Include implicit beans (service beans implicitly added by libraries). Applicable to Spring beans only. 

    * Show XML Infrastructure Beans: Include infrastructure beans (defined in XML files and related to the configuration). Applicable to Spring beans only. 




You can customize the colors for library and test beans in the IDE settings (`Ctrl+Alt+S`), under Appearance & Behavior | File Colors.

06 June 2025

[Build tool window](build-sync-tool-window.html)[CDI tool window](cdi-tool-window.html)
