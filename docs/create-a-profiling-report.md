[//]: # (Source: https://www.jetbrains.com/help/idea/create-a-profiling-report.html)
[//]: # (Downloaded: 2025-12-17 19:22:43)

## Prerequisites

You can use the default settings to profile most applications. Unless you are using Linux or want to use a custom profiler, no [configuration](custom-profiler-configurations.html) is required: everything works out-of-the-box.

For Linux and customizations, refer to [Custom profiler configurations](custom-profiler-configurations.html).

IntelliJ Profiler supports the following [run configurations](run-debug-configuration.html):

| Local process| [Run targets](run-targets.html)  
---|---|---  
[Application](run-debug-configuration.html#createExplicitly)| ![Feature is supported](https://resources.jetbrains.com/help/img/idea/2025.3/check_retina_bold_2.png)| ![Feature is supported](https://resources.jetbrains.com/help/img/idea/2025.3/check_retina_bold_2.png)  
[Spring Boot](run-debug-configuration-spring-boot.html)| ![Feature is supported](https://resources.jetbrains.com/help/img/idea/2025.3/check_retina_bold_2.png)| ![Feature is supported](https://resources.jetbrains.com/help/img/idea/2025.3/check_retina_bold_2.png)  
[Micronaut](micronaut.html)| ![Feature is supported](https://resources.jetbrains.com/help/img/idea/2025.3/check_retina_bold_2.png)| ![Feature is supported](https://resources.jetbrains.com/help/img/idea/2025.3/check_retina_bold_2.png)  
[Kotlin](run-debug-configuration-kotlin.html)| ![Feature is supported](https://resources.jetbrains.com/help/img/idea/2025.3/check_retina_bold_2.png)| ![Feature is supported](https://resources.jetbrains.com/help/img/idea/2025.3/check_retina_bold_2.png)  
[Ktor](ktor.html)| ![Feature is supported](https://resources.jetbrains.com/help/img/idea/2025.3/check_retina_bold_2.png)| ![Feature is supported](https://resources.jetbrains.com/help/img/idea/2025.3/check_retina_bold_2.png)  
[JUnit and Arquillian JUnit](run-debug-configuration-junit.html)| ![Feature is supported](https://resources.jetbrains.com/help/img/idea/2025.3/check_retina_bold_2.png)| ![Feature is supported](https://resources.jetbrains.com/help/img/idea/2025.3/check_retina_bold_2.png)  
[TestNG and Arquillian TestNG](run-debug-configuration-testng.html)| ![Feature is supported](https://resources.jetbrains.com/help/img/idea/2025.3/check_retina_bold_2.png)| ![Feature is supported](https://resources.jetbrains.com/help/img/idea/2025.3/check_retina_bold_2.png)  
[Maven](profile-maven-goals.html)| ![Feature is supported](https://resources.jetbrains.com/help/img/idea/2025.3/check_retina_bold_2.png)| ![Feature is not supported](https://resources.jetbrains.com/help/img/idea/2025.3/cross_retina.png)  
[Gradle](create-run-debug-configuration-gradle-tasks.html)| ![Feature is supported](https://resources.jetbrains.com/help/img/idea/2025.3/check_retina_bold_2.png)| ![Feature is not supported](https://resources.jetbrains.com/help/img/idea/2025.3/cross_retina.png)  
[Tomcat Server Local](run-debug-configuration-tomcat-server.html)| ![Feature is supported](https://resources.jetbrains.com/help/img/idea/2025.3/check_retina_bold_2.png)| ![Feature is not supported](https://resources.jetbrains.com/help/img/idea/2025.3/cross_retina.png)  
  
These configurations handle the prerequisites for you. If the required configuration is not on the list, you are welcome to create or vote for a request in [our issue tracker](https://youtrack.jetbrains.com/issues/IDEA?q=Subsystem:%20%\\7BJava.%20Profiler.%\\20CPU%\\7D).

For attaching to a process launched outside IntelliJ IDEA, make sure to enable [JMX](https://www.oracle.com/java/technologies/javase/docs-jmx-jsp.html).
