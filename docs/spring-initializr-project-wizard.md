[//]: # (Source: https://www.jetbrains.com/help/idea/spring-initializr-project-wizard.html)
[//]: # (Downloaded: 2025-12-17 20:03:04)

## Step 1. Basic project configuration

![First step of the New Spring Initializr Project wizard](https://resources.jetbrains.com/help/img/idea/2025.3/spring-new-project-initializr.png)

Server URL| Use the default <https://start.spring.io/> service or specify a custom instance. For more information, refer to [Creating your own instance](https://docs.spring.io/initializr/docs/current/reference/html/#create-instance).  
---|---  
Name| Specify a name for your project.  
Location| Specify the path to the directory in which you want to create the project. By default, the IDE creates a directory with the same name as the project.  
Language| Select the language that you want to use in your application.  
Type| Select the build tool to use for managing dependencies, testing, packaging, automating the build process, and so on: Gradle - Groovy, Gradle - Kotlin, or Maven.  
Group| Specify the unique group identifier for your project. It should preferably start with the reversed domain name you control (for example, `com.example`).  
Artifact| Specify a name for the artifact within the group, usually the project's name.  
Package name| Specify the root package of the project. This is usually a combination of the group and artifact names, for example: `com.example.springdemo`.  
JDK| From the JDK list, select the [JDK](sdk.html#jdk) that you want to use in your project.If the JDK is installed on your computer, but not defined in the IDE, select Add JDK and specify the path to the JDK home directory.If you don't have the necessary JDK on your computer, select Download JDK.  
Java| Select the Java version that the initializing service should use.  
Packaging| Select whether you want to package the app as a JAR or WAR.
