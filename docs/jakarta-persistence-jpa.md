[//]: # (Source: https://www.jetbrains.com/help/idea/jakarta-persistence-jpa.html)
[//]: # (Downloaded: 2025-12-17 19:30:10)

# Jakarta Persistence (JPA)

[Jakarta Persistence](https://jakarta.ee/specifications/persistence/) (JPA), formerly known as Java Persistence API, is a Java specification for managing relational data in [Java Enterprise](java-ee.html) applications.

### Enable the Jakarta EE: Persistence ​(JPA)​ plugin

This functionality relies on the [Jakarta EE: Persistence ​(JPA)​](https://plugins.jetbrains.com/plugin/20202) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the Jakarta EE: Persistence ​(JPA)​ plugin, and select the checkbox next to the plugin name.




IntelliJ IDEA provides the following:

  * Coding assistance specific to JPA.

  * A dedicated facet for managing the JPA configuration persistence.xml and object-relational mapping orm.xml files.

  * The [Persistence](persistence-tool-window.html) tool window for managing your JPA project items, creating configuration files and persistent classes, navigating to related source code in the editor, opening diagrams and consoles, and more.

  * Entity-relationship (ER) diagrams that you can access from the [Persistence](persistence-tool-window.html) tool window.

  * An ability to generate managed entity classes and object-relational mappings for them by importing a database schema or an EJB deployment descriptor file ejb-jar.xml.

  * The [JPA console](using-jpa-console.html) for writing and running JPQL queries, and analyzing the query results.




### Create a new Jakarta Enterprise project with JPA

Since JPA is part of Jakarta EE (formerly known as Java EE), you can add support for it to any [Java Enterprise/Jakarta Enterprise](java-ee.html) application.

  1. Click New Project on the Welcome screen or select File | New | Project.

  2. From the Generators list, select Jakarta EE.

  3. Name the new project, select a build tool, a language you want to use, and select the Web application project template.

  4. From the JDK list, select the [JDK](sdk.html#jdk) that you want to use in your project.

If the JDK is installed on your computer, but not defined in the IDE, select Add JDK and specify the path to the JDK home directory.

If you don't have the necessary JDK on your computer, select Download JDK.

![Creating new project with JPA support](https://resources.jetbrains.com/help/img/idea/2025.3/java_enterprise_new_project_step_1.png)
  5. On the next step of the wizard, select the Jakarta EE version to be supported.

  6. From the Dependencies list, select Persistence (JPA).

If you are not going to implement all the interfaces of the JPA specification yourself, you also need to include a persistence framework. By default, IntelliJ IDEA provides support for the following persistence frameworks:

     * EclipseLink is the reference implementation. Select it if you are just trying things out.

     * Hibernate is the most popular implementation. For more information, refer to [Hibernate](hibernate.html).

![New Jakarta EE project with JPA and Hibernate](https://resources.jetbrains.com/help/img/idea/2025.3/java_enterprise_new_project_step_2_hibernate.png)
  7. Click Create.




For more information about creating a Jakarta EE project, refer to [Tutorial: Your first Jakarta EE application](creating-and-running-your-first-jakarta-ee-application.html).

### Enable JPA support for an existing project

  1. Open the build file in the editor (pom.xml or build.gradle depending on the build tool that you use in your project).

  2. Add the following dependency, but make sure to change the version according to your project's requirements:

Jakarta EE
    

<dependency> <groupId>jakarta.persistence</groupId> <artifactId>jakarta.persistence-api</artifactId> <version>3.1.0</version> </dependency>

Java EE
    

<dependency> <groupId>javax.persistence</groupId> <artifactId>javax.persistence-api</artifactId> <version>2.2</version> <scope>provided</scope> </dependency>

Jakarta EE
    

implementation 'jakarta.persistence:jakarta.persistence-api:3.1.0' 

Java EE
    

compileOnly('javax.persistence:javax.persistence-api:2.2') 

  3. Press `Ctrl+Shift+O` to import the changes.

Once the dependency has been added, Jakarta Persistence features, such as the [Persistence](persistence-tool-window.html) tool window, become available right away.




For more information about working with build tools, refer to [Maven](maven-support.html) or [Gradle](gradle.html).

### Share facet settings

You can change and share settings by creating custom facets and adding a module file with the .iml extension to the version control system.

For example, to share a selected data source for JPA within your team, you can create a JPA facet and commit its settings.

  1. In the main menu, go to File | Project Structure or press `Ctrl+Alt+Shift+S`. Then select Modules.

  2. Make sure the module to which you want to add a facet is selected and click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg) above the list of modules. From the list of available facets, select JPA.

![Adding JPA facet](https://resources.jetbrains.com/help/img/idea/2025.3/add_jpa_facet.png)

The Descriptors section becomes available on the right.

  3. In the Descriptors section, click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.add.svg) and select a descriptor type. Create a new file or specify the path to an existing one.

  4. Reopen the project. After that, the changes will appear in the .iml file of the module to which you have added the facet. 

![JPA facet in module file](https://resources.jetbrains.com/help/img/idea/2025.3/jpa_facet_iml.png)
  5. [Add the .iml file](adding-files-to-version-control.html#add-files-to-vcs) to your version control system.




18 November 2025

[Jakarta Server Faces (JSF)](javaserver-faces-jsf.html)[Persistence tool window](persistence-tool-window.html)
