[//]: # (Source: https://www.jetbrains.com/help/idea/running-a-java-app-in-a-container.html)
[//]: # (Downloaded: 2025-12-17 19:59:15)

# Run and debug a Java application with Docker

You can use Docker to run and debug a Java application in a container with a specific runtime environment. This tutorial describes how to create a [Docker run target](docker-run-targets.html) with OpenJDK 17 for a simple Java application.

Before you begin, install and run Docker, enable the Docker plugin, and connect to the Docker daemon in IntelliJ IDEA. For more information, refer to [Getting started with Docker in IntelliJ IDEA](docker.html#connect_to_docker).

### Create a new Java project

The sample application for this tutorial will consist of a single HelloWorld.java file, which prints `Hello, World!` to the console and exits.

  1. In the main menu, go to File | New | Project.

  2. In the New Project wizard, select Java from the list on the left.

  3. In the New Project dialog, name the project `DockerHelloWorld`.

![New Java project](https://resources.jetbrains.com/help/img/idea/2025.3/docker_new_java_project.png)
  4. Create the main Java class file HelloWorld.java in the src directory.

To do this, in the Project tool window, right-click the src directory, point to New and click Java Class. In the New Java Class dialog, type `HelloWorld` and press `Enter`.

Paste the following code into the new file:

public class HelloWorld { public static void main(String[] args) { System.out.println("Hello, World!"); } } 

  5. Try to compile and run the application.

Click ![The Run gutter icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.execute.svg) in the gutter and select Run 'HelloWorld.main()'.

You should see `Hello, World!` printed to the console of the Run tool window.

![Running the new Java application locally](https://resources.jetbrains.com/help/img/idea/2025.3/docker_new_java_project_run.png)



By default, IntelliJ IDEA creates a [run configuration](run-debug-configuration.html) that compiles and executes your application locally. You can configure different [run targets](run-targets.html) for it, including remote machines via SSH connections and Docker containers.

### Run the Java application on a Docker run target

  1. In the main menu, go to Run | Edit Configurations.

  2. Select the run configuration that compiles and executes your application, expand the Run on list, and select Docker.

![Add a Docker run target to run configuration](https://resources.jetbrains.com/help/img/idea/2025.3/docker_add_run_target.png)
  3. On the first step of the New Target: Docker wizard, select Pull or use existing, and specify `openjdk` as the name of the image to pull.

  4. On the second step, Docker will pull the specified image.

  5. On the third step, click Create to add the new Docker run target.

  6. Click Apply to save the changes to the run configuration.

  7. Start the run configuration to compile and execute your application on the latest OpenJDK container. For more information, refer to [Run applications](running-applications.html).




### Debug the Java application

  1. Open HelloWorld.java and click line number 3 with `System.out.println("Hello, World!");` to [put a breakpoint](using-breakpoints.html) on this line.

  2. Select your application's run configuration but instead of running it, start the debugger with ![the Debug button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.startDebugger.svg). For more information, refer to [Start the debugger session](starting-the-debugger-session.html).




This will compile and execute the application in debug mode, and IntelliJ IDEA will halt execution at the specified breakpoint: just before it prints out to the console.

![Debugging Java app on a Docker run target](https://resources.jetbrains.com/help/img/idea/2025.3/docker_run_target_debug.png)

11 October 2024

[Dockerize a Java application](dockerize-java-app.html)[Run and debug a Spring Boot application using Docker Compose](run-and-debug-a-spring-boot-application-using-docker-compose.html)
