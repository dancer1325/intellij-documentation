[//]: # (Source: https://www.jetbrains.com/help/idea/context-and-dependency-injection-cdi.html)
[//]: # (Downloaded: 2025-12-17 19:22:27)

# Contexts and Dependency Injection (CDI)

[Jakarta Contexts and Dependency Injection](https://jakarta.ee/specifications/cdi/) (CDI) is a specification for declarative dependency injection and supporting services.

### Enable the Jakarta EE: Contexts and Dependency Injection (CDI) plugin

This functionality relies on the [Jakarta EE: Contexts and Dependency Injection (CDI)](https://plugins.jetbrains.com/plugin/20204) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

The Jakarta EE: Contexts and Dependency Injection (CDI) plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the Jakarta EE: Contexts and Dependency Injection (CDI) plugin, and select the checkbox next to the plugin name.




You can enable CDI support when creating a new project or module, or add CDI support to an existing module.

### Create a new Jakarta Enterprise project with CDI

Since CDI is part of Jakarta EE (formerly known as Java EE), you can add support for it to any [Java Enterprise/Jakarta Enterprise](java-ee.html) application.

  1. Click New Project on the Welcome screen or select File | New | Project.

  2. From the Generators list, select Jakarta EE.

  3. Name the new project, select a build tool, a language you want to use, and select the Web application project template.

  4. From the JDK list, select the [JDK](sdk.html#jdk) that you want to use in your project.

If the JDK is installed on your computer, but not defined in the IDE, select Add JDK and specify the path to the JDK home directory.

If you don't have the necessary JDK on your computer, select Download JDK.

![Creating new project with CDI support](https://resources.jetbrains.com/help/img/idea/2025.3/java_enterprise_new_project_step_1.png)
  5. On the next step of the wizard, select the Jakarta EE version to be supported.

  6. From the Dependencies list, select Contexts and Dependency Injection (CDI).

![Creating new project with CDI support](https://resources.jetbrains.com/help/img/idea/2025.3/java_enterprise_new_project_step_2_cdi.png)
  7. Click Create.




For more information about creating a Jakarta EE project, refer to [Tutorial: Your first Jakarta EE application](creating-and-running-your-first-jakarta-ee-application.html).

### Enable CDI support for an existing project

  1. Open the build file in the editor (pom.xml or build.gradle depending on the build tool that you use in your project).

  2. Add the following dependency, but make sure to change the version according to your project's requirements:

Jakarta EE
    

<dependency> <groupId>jakarta.enterprise</groupId> <artifactId>jakarta.enterprise.cdi-api</artifactId> <version>4.0.1</version> </dependency>

Java EE
    

<dependency> <groupId>javax.enterprise</groupId> <artifactId>cdi-api</artifactId> <version>2.0.SP1</version> <scope>provided</scope> </dependency>

Jakarta EE
    

implementation 'jakarta.enterprise:jakarta.enterprise.cdi-api:4.0.1' 

Java EE
    

compileOnly('org.apache.deltaspike.cdictrl:deltaspike-cdictrl-api:1.9.5') 

  3. Press `Ctrl+Shift+O` to import the changes.




For more information about working with build tools, refer to [Maven](maven-support.html) or [Gradle](gradle.html).

09 August 2024

[Enterprise application support](enabling-java-ee-application-support.html)[Jakarta Server Faces (JSF)](javaserver-faces-jsf.html)
