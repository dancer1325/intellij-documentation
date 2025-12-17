[//]: # (Source: https://www.jetbrains.com/help/idea/docker-tutorial-tomcat-debug.html)
[//]: # (Downloaded: 2025-12-17 19:25:15)

# Deploy and debug a Java web application inside a container running Tomcat

You can use a Docker container to run an application server for deploying and debugging your Java web application. This is a great way to test and debug web applications on various versions of the application server that reproduce various environments.

This tutorial describes how to use a Docker Compose file to run a Docker container with the web application deployed to the Tomcat application server and all necessary configuration for debugging: exposing the debugger port, bind mounting the output directory with the WAR file to Tomcat in the container, and opening the debugger socket.

Before you begin, install and run Docker, enable the Docker plugin, and connect to the Docker daemon in IntelliJ IDEA. For more information, refer to [Getting started with Docker in IntelliJ IDEA](docker.html#connect_to_docker).

### Clone the sample project

The source code of the application is hosted on GitHub at <https://github.com/IdeaUJetBrains/Tomcat_docker_debug>

  1. In the main menu, go to File | New | Project from Version Control.

  2. Specify the URL of the repository and click Clone.

  3. If necessary, agree to open the cloned project in a new window.


![Clone the repository with the sample project](https://resources.jetbrains.com/help/img/idea/2025.3/docker_compose_tomcat_debug_tutorial_step1.png)

### Build the WAR artifact

  1. In the main menu, go to Build | Build Artifacts

  2. Select tomcat_docker_debug:war exploded and build it.


![Build the WAR artifact](https://resources.jetbrains.com/help/img/idea/2025.3/docker_compose_tomcat_debug_tutorial_step2.png)

The built artifact appears in the project root under target/.

### Run the application using Docker Compose

  1. Open docker-compose.yml.

  2. Click ![docker compose up](https://resources.jetbrains.com/help/img/idea/2025.3/app.runConfigurations.testState.run_run.svg) in the gutter next to `services`.




This creates a Docker Compose run configuration that runs the application in a container as a separate Docker Compose service defined in docker-compose.yml.

Image
    

This tutorial uses the image `tomcat:10.0-jdk17`, which is compatible with Jakarta EE 9.1. If your application uses Jakarta EE 10, run it on Tomcat 10.1. For Java EE 8, use Tomcat 9 and earlier versions.

Ports
    

To access the application from your host machine, Docker Compose exposes port 8080 in the container as port 8888 on the host. It also exposes port 5005 in the container as port 5005 on the host for the debugger.

Volumes
    

Instead of copying the WAR artifact to the container, Docker Compose bind mounts the application output directory ./target to the Tomcat directory in the container: /usr/local/tomcat/webapps.

Environment variables
    

To attach the debugger, Docker Compose sets the `JAVA_OPTS` environment variable to the following: 

-agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=*:5005

Command
    

Docker Compose overrides the default command declared by the Tomcat image and sets it to `catalina.sh run`.

### Check that the application is running

  1. Open the container log and make sure it ends with a message that Tomcat has started.

  2. Open the following URL in your browser: <http://localhost:8888/Tomcat_docker_debug-1.0-SNAPSHOT/api/hello-world>. It should return a page with `Hello, World!`


![Hello, World! response from the Java web application](https://resources.jetbrains.com/help/img/idea/2025.3/docker_compose_tomcat_debug_tutorial_step3.png)

### Attach the debugger

  1. Run the Remote JVM Debug configuration named `remote_tomcat_debug`, which attaches the debugger remotely.

  2. Open src/main/java/com/example/tomcat_docker_debug/HelloResource.java and set a breakpoint in the `hello()` method on the line with `return "Hello, World!";`

![Set a breakpoint for the endpoint](https://resources.jetbrains.com/help/img/idea/2025.3/docker_compose_tomcat_debug_tutorial_step4.png)
  3. Refresh or open the REST endpoint again: <http://localhost:8888/Tomcat_docker_debug-1.0-SNAPSHOT/api/hello-world>. This time, it should hit the breakpoint inside the mentioned method.




For convenience, you can configure a `Before launch` task in the `remote_tomcat_debug` run configuration so that it first starts the `docker_compose` configuration. However, there is an issue that Docker Compose needs some time to start the service, and remote JVM debug does not wait for the service. There is a fix for this that will be available in the next major release: 2023.3. For more information, refer to [IDEA-172781](https://youtrack.jetbrains.com/issue/IDEA-172781).

15 July 2024

[Deploy a Java web application inside an application server container](deploying-a-web-app-into-an-app-server-container.html)[Docker troubleshooting](docker-troubleshooting.html)
