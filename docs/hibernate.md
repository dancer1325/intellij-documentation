[//]: # (Source: https://www.jetbrains.com/help/idea/hibernate.html)
[//]: # (Downloaded: 2025-12-17 19:28:44)

# Hibernate

[Hibernate](http://hibernate.org/) is an object-relational mapping framework that implements the [Jakarta Persistence (JPA)](jakarta-persistence-jpa.html) specification.

IntelliJ IDEA provides the following:

  * Coding assistance specific to Hibernate.

  * A dedicated facet for managing the Hibernate configuration hibernate.cfg.xml.

  * Additions to the [Persistence](persistence-tool-window.html) tool window for managing your Hibernate items, creating configuration files and persistent classes, navigating to related source code in the editor, opening diagrams and consoles, and more.

  * Entity-relationship (ER) diagrams that you can access from the [Persistence](persistence-tool-window.html) tool window.

  * An ability to generate managed entity classes and object-relational mappings for them by importing a database schema or an EJB deployment descriptor file ejb-jar.xml.

  * The [Hibernate console](working-with-the-hibernate-console.html) for writing and running HQL queries, and analyzing the query results.




### Create a new Jakarta Enterprise project with Hibernate

  1. Click New Project on the Welcome screen or select File | New | Project.

  2. From the Generators list, select Jakarta EE.

  3. Name the new project, select a build tool, a language you want to use, and select the Web application project template.

  4. From the JDK list, select the [JDK](sdk.html#jdk) that you want to use in your project.

If the JDK is installed on your computer, but not defined in the IDE, select Add JDK and specify the path to the JDK home directory.

If you don't have the necessary JDK on your computer, select Download JDK.

![Creating new project with Hibernate support](https://resources.jetbrains.com/help/img/idea/2025.3/java_enterprise_new_project_step_1.png)
  5. On the next step of the wizard, select the Jakarta EE version to be supported.

  6. From the Dependencies list, select the Persistence (JPA) specification and Hibernate as the implementation.

![New Jakarta EE project with JPA and Hibernate](https://resources.jetbrains.com/help/img/idea/2025.3/java_enterprise_new_project_step_2_hibernate.png)
  7. Click Create.




For more information about creating a Jakarta EE project, refer to [Tutorial: Your first Jakarta EE application](creating-and-running-your-first-jakarta-ee-application.html).

IntelliJ IDEA creates the default project structure with the JPA [facet](adding-support-for-frameworks-and-technologies.html) and all the necessary libraries as external dependencies, such as `javax.persistence` for the JPA specification and `org.hibernate` for the Hibernate framework. If you specified an [application server](application-servers-support.html), IntelliJ IDEA will also create a run configuration to start the server, build and deploy the artifact.

### Enable Hibernate support for an existing project

  1. Open the build file in the editor (pom.xml or build.gradle depending on the build tool that you use in your project).

  2. Add the following dependency, but make sure to change the version according to your project's requirements:

<dependency> <groupId>org.hibernate</groupId> <artifactId>hibernate-core</artifactId> <version>5.6.0.Final</version> </dependency>

implementation('org.hibernate:hibernate-core:5.6.1.Final') 

  3. Press `Ctrl+Shift+O` to import the changes.




For more information about working with build tools, refer to [Maven](maven-support.html) or [Gradle](gradle.html).

11 October 2024

[JPA console](using-jpa-console.html)[Hibernate console](working-with-the-hibernate-console.html)
