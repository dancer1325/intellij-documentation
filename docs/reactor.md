[//]: # (Source: https://www.jetbrains.com/help/idea/reactor.html)
[//]: # (Downloaded: 2025-12-17 19:56:45)

## Add Reactor support

Reactor works with Kotlin, Java 8 and later, and with Android SDK 26 (Android O) and later.

There are several options for adding Reactor support to your project: you can add the necessary dependencies to the build file of Maven or Gradle projects, or you can manually download the Reactor library. For Spring Boot applications, IntelliJ IDEA allows you to add the required dependencies when you create a new project.

### Add Reactor to a Maven project

For Maven projects, it's recommended that you import the [Bill of Materials (BOM)](https://projectreactor.io/docs/core/release/reference/#getting-started-understanding-bom) together with the core, as it ensures that Reactor components work well together.

  1. In the `pom.xml` file, add the following dependency to import the BOM: 

<dependencyManagement> <dependencies> <dependency> <groupId>io.projectreactor<groupId> <artifactId>reactor-bom<artifactId> <version>Dysprosium-SR1<version> <type>pom</type> <scope>import<scope> <dependency> <dependencies> <dependencyManagement>

  2. Add the following dependency to import Reactor: 

<dependencies> <dependency> <groupId>io.projectreactor<groupId> <artifactId>reactor-core<artifactId> <dependency> <dependencies>




### Add Reactor to Gradle (Gradle 5.0 and later)

For Gradle projects, it's recommended that you import the [Bill of Materials (BOM)](https://projectreactor.io/docs/core/release/reference/#getting-started-understanding-bom) together with the core, as it ensures that Reactor components work well together.

  * In the `build.gradle`, add the following dependencies: 

dependencies { // import BOM implementation platform('io.projectreactor:reactor-bom:Dysprosium-SR1') // add dependencies without a version number implementation 'io.projectreactor:reactor-core' } 




### Add Reactor to Gradle (Gradle 4.x and earlier)

For Gradle projects, it's recommended that you import the [Bill of Materials (BOM)](https://projectreactor.io/docs/core/release/reference/#getting-started-understanding-bom) together with the core, as it ensures that Reactor components work well together.

Previous Gradle versions don't support the BOM, however, you can use the Spring [gradle-dependency-management](https://github.com/spring-gradle-plugins/dependency-management-plugin) plugin to import it to your project.

  1. Obtain the plugin from Gradle Plugin Portal by adding the following code to `build.gradle`:

plugins { id "io.spring.dependency-management" version "1.0.6.RELEASE" } 

Use the latest available version; we used the 1.0.6.RELEASE version as an example.

  2. Import the BOM by adding the following code: 

dependencyManagement { imports { mavenBom "io.projectreactor:reactor-bom:Dysprosium-SR1" } } 

  3. Add Reactor support: 

dependencies { compile 'io.projectreactor:reactor-core' } 




### Add the Reactor library to a project

If you build your project with the native IDE builder, you can add Reactor support as a library.

  1. In the main menu, go to File | Project Structure `Ctrl+Alt+Shift+S` or click ![the Project Structure button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.projectStructure.svg) on the toolbar.

  2. Select Libraries, click ![the New Project Library button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg), and then select From Maven.

  3. In the dialog that opens, specify the library artifact `io.projectreactor:reactor-core:3.1.06.RELEASE` and click OK.

Use the latest available version; we used the 3.1.6.RELEASE version as an example.

![Adding the Reactor library from Maven](https://resources.jetbrains.com/help/img/idea/2025.3/reactor-from-maven.png)



### Create a new Spring Boot project with Reactor

  1. Launch IntelliJ IDEA.

If the Welcome screen opens, click New Project.

Otherwise, go to File | New | Project in the main menu.

  2. Select Spring Initializr from the left pane.

     * Click ![the Configure icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) to enter the URL of the service that you want to use, or leave the default one.

     * Specify a name and location for your project and configure project metadata: select a language, a build tool, and specify an artifact ID.

     * From the JDK list, select the [JDK](sdk.html#jdk) that you want to use in your project.

If the JDK is installed on your computer, but not defined in the IDE, select Add JDK and specify the path to the JDK home directory.

If you don't have the necessary JDK on your computer, select Download JDK.

If you want to build your project on a Java version different from your project JDK version, you can select it here.

![Creating a new Spring Boot project with Reactor](https://resources.jetbrains.com/help/img/idea/2025.3/reactor-new-project.png)

Click Next.

  3. On the next step of the wizard, from the Dependencies list, select Spring Reactive Web and click Create.

![Specifying the Reactive Web dependency](https://resources.jetbrains.com/help/img/idea/2025.3/reactor-dependency.png)


