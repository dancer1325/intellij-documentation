[//]: # (Source: https://www.jetbrains.com/help/idea/micronaut.html)
[//]: # (Downloaded: 2025-12-17 19:32:22)

# Micronaut

[Micronaut](https://micronaut.io/) is a modern Java framework for writing microservice and serverless applications. IntelliJ IDEA provides the following:

Micronaut support is limited in IntelliJ IDEA without the Ultimate subscription.

IntelliJ IDEA provides the following:

  * A dedicated project creation wizard based on [launch.micronaut.io](https://launch.micronaut.io/).

  * A dedicated run configuration for Micronaut applications.




IntelliJ IDEA with the Ultimate subscription additionally provides the following:

  * Coding assistance specific to the Micronaut API and the configuration file parameters. For example, when [writing query methods](https://micronaut-projects.github.io/micronaut-data/latest/guide/#querying), generating HTTP requests for defined endpoints, and so on.

  * Integration with the [Beans](beans-tool-window.html) and [Endpoints](endpoints-tool-window.html) tool windows.




### Create a new Micronaut project

  1. Launch IntelliJ IDEA.

If the Welcome screen opens, click New Project.

Otherwise, go to File | New | Project in the main menu.

  2. Select Micronaut from the left pane.

     * Click ![the Configure icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) to enter the URL of the service that you want to use, or leave the default one.

     * Specify a name and location for your project and configure project metadata: select a language, a build tool, and specify an artifact ID.

     * From the JDK list, select the [JDK](sdk.html#jdk) that you want to use in your project.

If the JDK is installed on your computer, but not defined in the IDE, select Add JDK and specify the path to the JDK home directory.

If you don't have the necessary JDK on your computer, select Download JDK.

If you want to build your project on a Java version different from your project JDK version, you can select it here.

![New Micronaut project wizard](https://resources.jetbrains.com/help/img/idea/2025.3/micronaut-new-project.png)

Click Next.

  3. On the next step of the wizard, from the Features list, select the necessary options and click Create.




The generated project contains only the main `Application` class and everything necessary to run the application. IntelliJ IDEA recognizes it and adds ![the Run icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.gutter.run.svg) to the gutter, which you can click to run the application.

![The default Micronaut application main class](https://resources.jetbrains.com/help/img/idea/2025.3/micronaut-default-main-class.png)

However, an empty project is boring. Let's make the application return `Hello World!` in response to an HTTP GET request.

### Add a Micronaut HTTP controller

  1. Right-click the directory with the main class (be default, it is src/main/java/com/example) and select New | Java Class.

  2. Type the name of the class `HelloController` and press `Enter`.

  3. Copy the following code into the created file:

package com.example; import io.micronaut.http.MediaType; import io.micronaut.http.annotation.Controller; import io.micronaut.http.annotation.Get; import io.micronaut.http.annotation.Produces; @Controller("/hello") public class HelloController { @Get(produces = MediaType.TEXT_PLAIN) public String sayHello() { return "Hello World!"; } } 

     * The `@Controller` annotation defines the class as an HTTP controller mapped to the `/hello` endpoint.

     * The `@Get` annotation maps all HTTP GET requests for this endpoint to the `sayHello()` method and sets the `Content-Type` of the response to `text/plain`.

     * The `sayHello()` method returns the string `Hello World!`.




IntelliJ IDEA recognizes the HTTP controller and marks it with ![The HTTP Controller icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.icons.cdi.newui.bean%4014x14.svg) in the gutter. You can also click ![The Open in HTTP Client icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.icons.web.newui.requestMapping%4014x14.svg) to generate an HTTP request for the endpoint and open it in a separate [HTTP client](http-client-in-product-code-editor.html) editor tab. IntelliJ IDEA provides other gutter icons, for example:

  * ![The Navigate to event listeners icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.icons.cdi.newui.listener%4014x14.svg) Navigate to event listeners

  * ![The Navigate to event publisher icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.icons.cdi.newui.publisher%4014x14.svg) Navigate to event publisher

  * ![The Navigate to the autowired dependencies icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.icons.cdi.newui.showAutowiredDependencies%4014x14.svg) Navigate to the autowired dependencies




To see all the endpoints defined in your application, open the [Endpoints](endpoints-tool-window.html) tool window. For example, here is the `/hello` endpoint:

![The Endpoints tool window with the sample /hello endpoint](https://resources.jetbrains.com/help/img/idea/2025.3/micronaut-hello-endpoint.png)

### Run the Micronaut application

IntelliJ IDEA creates a Micronaut run configuration that executes the necessary Maven goal or Gradle task.

  * Select the Micronaut run configuration in the main toolbar and click ![the Run button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.gutter.run.svg) or press `Shift+F10`.

Alternatively, you can press `Alt+Shift+F10` and select the necessary run configuration.

If successful, you should see the output log in the Run tool window.

![Micronaut application running in the Run tool window](https://resources.jetbrains.com/help/img/idea/2025.3/micronaut-run-tool-window.png)



By default, the application starts on <http://localhost:8080>. Open this address in a web browser, and you will see the standard error response because the application root doesn't handle GET requests:

{"message":"Page Not Found","_links":{"self":{"href":"/","templated":false}}}

However, the application has an [HTTP controller](#controller) that responds to GET requests. If you open the <http://localhost:8080/hello> endpoint, the application will respond with `Hello World!`.

### Quickly create a connection to a database

Using the Database Tools and SQL plugin, IntelliJ IDEA lets you create and manage [connections to databases](connecting-to-a-database.html).

In a Micronaut project, you can instantly create it from your application properties file.

  1. Open an application.properties or application.yml file. If it contains datasource-related properties (for example, `mongodb.uri` or `redis.host`) , the datasource icon ![Datasource icon](https://resources.jetbrains.com/help/img/idea/2025.3/javaee-persistence-impl.icons.expui.add-db-from-config.svg) will be displayed in the gutter.

  2. Click ![Datasource icon](https://resources.jetbrains.com/help/img/idea/2025.3/javaee-persistence-impl.icons.expui.add-db-from-config.svg). This will open the data source creation form with datasource parameters (such as URL, username, or database name) populated based on data from your configuration file.

If the data source is already configured, the datasource icon ![](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.dbms.svg) is displayed instead. Click it to open the datasource in the Database tool window.

![Create data source window](https://resources.jetbrains.com/help/img/idea/2025.3/micronaut_create_datasource_from_properties.png)



Below is the list of databases for which this action is available:

  * Amazon Redshift

  * Apache Cassandra

  * Apache Derby

  * Couchbase

  * H2

  * HSQLDB

  * IBM Db2

  * MariaDB

  * Microsoft SQL Server

  * MongoDB

  * MySQL

  * Oracle Database

  * PostgreSQL

  * Redis

  * SQLite

  * Sybase




For more details on data source parameters, refer to [Data sources](managing-data-sources.html).

26 November 2025

[Quarkus run configuration](quarkus-run-configuration.html)[Message queues](message-queues.html)
