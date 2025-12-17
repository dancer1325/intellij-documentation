[//]: # (Source: https://www.jetbrains.com/help/idea/run-and-debug-a-spring-boot-application-using-docker-compose.html)
[//]: # (Downloaded: 2025-12-17 19:57:52)

# Run and debug a Spring Boot application using Docker Compose

You can use IntelliJ IDEA to run and debug a [Spring Boot](https://spring.io/projects/spring-boot) application running in multiple Docker containers under Docker Compose. This tutorial describes how to run two Docker Compose services inside containers in the same virtual network: a simple Spring Boot application and a MySQL database. The application can receive GET requests that add entries to the database. This tutorial also describes how you can set breakpoints and debug your application.

Before you begin, install and run Docker, enable the Docker plugin, and connect to the Docker daemon in IntelliJ IDEA. For more information, refer to [Getting started with Docker in IntelliJ IDEA](docker.html#connect_to_docker).

For features related to Spring, refer to [Enable Spring support in IntelliJ IDEA](spring-support.html#check_required_spring_plugins).

### Clone the sample project

The source code of the application is hosted on GitHub at <https://github.com/IdeaUJetBrains/SpringBootDockerDemoDebug>.

  1. In the main menu, go to File | New | Project from Version Control.

  2. Specify the URL of the repository and click Clone.

  3. If necessary, agree to open the cloned project in a new window.


![Clone sample Spring Boot project for Docker](https://resources.jetbrains.com/help/img/idea/2025.3/docker_spring_boot_clone.png)

### Prepare the Spring Boot run configuration

The project should have the DemoApplication configuration, which runs the Spring Boot application. By default, it runs locally, but you need to run it on the container from the Docker Compose `java` service.

If you don't have the DemoApplication configuration, open the DemoApplication.java file and click ![the Run icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.execute.svg) in the gutter. The application will not actually run without a proper Java runtime and the required database, but this will automatically create the DemoApplication configuration for you.

  1. In the main menu, go to Run | Edit Configurations.

  2. In the Run/Debug Configurations dialog, select the DemoApplication configuration, expand the Run on list, and select Docker Compose under Create New Targets. 

![Add new Docker Compose target](https://resources.jetbrains.com/help/img/idea/2025.3/docker_spring_boot_demoapp_new_target.png)
  3. Select the docker-compose.yml file, then the `java` service, and click Next. 

![Add Docker Compose run target with Java service](https://resources.jetbrains.com/help/img/idea/2025.3/docker_spring_boot_add_java_run_target.png)
  4. After IntelliJ IDEA builds the target image and detects the Java home path, click Next.

  5. Check the detected Java home path and version and click Create.

  6. Make sure that the new `java` service run target is selected and apply the changes to the DemoApplication configuration. 

![DemoApplication with new run target](https://resources.jetbrains.com/help/img/idea/2025.3/docker_spring_boot_demoapp_with_target.png)



You can configure a run target from a Dockerfile or an image, but in this tutorial we are using Docker Compose to run two services in the same network, so that the Java application in one service can access the database in the other service.

### Prepare the database run configuration

You need to run the database for the application from the `db` service defined in the same docker-compose.yml file. Create a run configuration for it and then configure to run it before the Spring Boot application.

  1. In the Run/Debug Configurations dialog, click Add New Configuration ![the Add New Configuration button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select Docker Compose.

  2. Give this configuration a descriptive name like `DatabaseService`, specify the docker-compose.yml file, and then add the `db` service. 

![Docker Compose configuration for the database service](https://resources.jetbrains.com/help/img/idea/2025.3/docker_spring_boot_compose_db_config.png)
  3. Apply the changes to the new configuration and select the DemoApplication configuration.

  4. In the DemoApplication configuration, click Modify options, select Add before launch task, then click Run Another Configuration, and add the new Docker Compose configuration to run the database service before the main application. 

![DemoApplication run config with Docker Compose as a Before Launch task](https://resources.jetbrains.com/help/img/idea/2025.3/docker_spring_boot_add_before_launch_task.png)
  5. After you apply the changes, run the DemoApplication configuration.




### Run the application

When you run the DemoApplication configuration, IntelliJ IDEA will first start the `db` Docker Compose service and make sure that the database is healthy. Then it will start the `java` service as a run target for the Spring Boot application. Finally, it will use the Java runtime from the run target for the Spring Boot application. If everything is correct, you should see the following output:

![Console output after successfully running the Spring Boot application](https://resources.jetbrains.com/help/img/idea/2025.3/docker_spring_boot_run_console_output.png)

  1. Note the random local port number that Docker forwards to port 8080 in the container where the application is running. In the example above, it is 54123.

  2. You can access the application and list the entities stored in the database at <http://localhost:54123/entitybus> (replace the port number with whatever Docker assigns in your case).

  3. To add a random entity to the database, send a GET request to <http://localhost:54123/entitybus/post>.


![Execute a GET request](https://resources.jetbrains.com/help/img/idea/2025.3/docker_spring_boot_get_request.png)

### Connect to the database

If you want, you can connect to the running database at jdbc:mysql://0.0.0.0:13306/DOCKERDB.

  * Open the [Database](database-tool-window.html) tool window and add a MySQL data souce with the following settings:

Host
    

`localhost`

Port
    

`13306`

User
    

`root`

Password
    

`root`

Database
    

`DOCKERDB`


![Connect to MySQL](https://resources.jetbrains.com/help/img/idea/2025.3/docker_spring_boot_mysql_connection.png)

### Debug the application

  1. Run DemoApplication in debug mode. For example, with the run configuration selected, click the Debug button ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.run.debug.svg) in the main toolbar.

  2. Open the EntitybusController.java file and set a breakpoint somewhere inside the `postEntity()` method. For example, on line number 27.

  3. Open <http://localhost:54123/entitybus/post> in your browser (or whatever port Docker assigned in your case).




The debugger should suspend execution at the breakpoint, and you can examine the current state, such as variable values and frames.

![Spring Boot application suspended at breakpoint](https://resources.jetbrains.com/help/img/idea/2025.3/docker_spring_boot_debug_suspended.png)

11 October 2024

[Run and debug a Java application with Docker](running-a-java-app-in-a-container.html)[Deploy a Java web application inside an application server container](deploying-a-web-app-into-an-app-server-container.html)
