[//]: # (Source: https://www.jetbrains.com/help/idea/preparing-for-rest-development.html)
[//]: # (Downloaded: 2025-12-17 19:34:08)

# Get started with REST development

At the IntelliJ IDEA level, the RESTful Web Services development support is based on the Jakarta EE: RESTful Web Services (JAX-RS) [plugin](managing-plugins.html). This plugin is bundled with IntelliJ IDEA Ultimate and enabled by default.

### Make sure that the RESTful Web Services plugin is enabled

  1. In the Settings dialog (`Ctrl+Alt+S`) , select Plugins.

  2. Switch to the Installed tab and make sure that the Jakarta EE: RESTful Web Services (JAX-RS) plugin is enabled.

If the plugin is disabled, select the checkbox next to it.

  3. Apply the changes and close the dialog. Restart the IDE if prompted.




### Enable REST support when creating a project

  1. Click New Project on the Welcome screen or select File | New | Project.

  2. From the Generators list, select Jakarta EE.

  3. Name the new project, select a build tool, a language you want to use, and select the REST service project template.

  4. Select the Create Git repository option to place the new project under version control.

  5. From the JDK list, select the [JDK](sdk.html#jdk) that you want to use in your project.

If the JDK is installed on your computer, but not defined in the IDE, select Add JDK and specify the path to the JDK home directory.

If you don't have the necessary JDK on your computer, select Download JDK.

![Creating new project with REST support](https://resources.jetbrains.com/help/img/idea/2025.3/new-project-restful.png)
  6. On the next step of the wizard, select the Java EE version to be supported.

  7. From the Dependencies list, select RESTful Web Services (JAX-RS).

  8. Click Create.




### Enabling REST support for a Maven project

  1. Open the pom.xml file and add the necessary dependency.

The dependency should correspond to the Java version that is used in your project. For example, for Java EE, add:

<dependency> <groupId>javax.ws.rs</groupId> <artifactId>javax.ws.rs-api</artifactId> <version>2.1.1</version> </dependency>

If your project uses Jakarta EE, add:

<dependency> <groupId>jakarta.ws.rs</groupId> <artifactId>jakarta.ws.rs-api</artifactId> <version>3.0.0</version> <scope>provided</scope> </dependency>

  2. Press `Ctrl+Shift+O` to import the changes.




### Enabling REST support for a Gradle project

  1. Open the build.gradle file and add the necessary dependency.

The dependency should correspond to the Java version that is used in your project. For example, for Java EE, add:

implementation 'javax.ws.rs:javax.ws.rs-api:2.1.1' 

If your project uses Jakarta EE, add:

implementation 'jakarta.ws.rs:jakarta.ws.rs-api:3.0.0' 

  2. Press `Ctrl+Shift+O` to import the changes.




For more information about working with build tools, refer to [Maven](maven-support.html) or [Gradle](gradle.html).

11 October 2024

[Tutorial: Your first RESTful web service](creating-and-running-your-first-restful-web-service.html)[Coding assistance for REST development](coding-assistance-for-rest-development.html)
