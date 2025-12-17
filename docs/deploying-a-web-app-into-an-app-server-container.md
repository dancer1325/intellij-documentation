[//]: # (Source: https://www.jetbrains.com/help/idea/deploying-a-web-app-into-an-app-server-container.html)
[//]: # (Downloaded: 2025-12-17 19:24:36)

# Deploy a Java web application inside an application server container

You can use Docker to run an application server (Tomcat, Wildfly, and so on) and deploy your Java web applications in it. This tutorial describes how to create a simple Java web application, build a deployable web application resource (WAR) file, and then deploy it inside application server running as a Docker container.

Before you begin, install and run Docker, enable the Docker plugin, and connect to the Docker daemon in IntelliJ IDEA. For more information, refer to [Getting started with Docker in IntelliJ IDEA](docker.html#connect_to_docker).

### Create a Java web application

  1. In the main menu, go to File | New | Project.

  2. In the New Project dialog, select Jakarta EE and do the following:

     * Enter a name for your project: `DockerJavaWebApp`

     * Select the Web application template

     * Select a recent JDK for the project (OpenJDK 17 is a good choice)

![New Java Enterprise project wizard](https://resources.jetbrains.com/help/img/idea/2025.3/docker_java_web_app_step1.png)

Click Next to continue.

  3. On the next step of the wizard, select Jakarta EE 9 the Web Profile specification.

![New Java Enterprise project wizard](https://resources.jetbrains.com/help/img/idea/2025.3/docker_java_web_app_step2.png)

Click Create.




IntelliJ IDEA generates a default project with a Java web application that has the index.jsp home page and the `HelloServlet.java` class that responds to requests at /hello-servlet.

### Build a WAR artifact

After IntelliJ IDEA creates the new project, build a WAR artifact to deploy to the application server.

  1. In the main menu, go to Build | Build Artifacts.

  2. In the Build Artifact dialog, select to build the DockerJavaWebApp:war artifact.




You should see the artifact target/DockerJavaWebApp-1.0-SNAPSHOT.war.

![Created WAR artifact](https://resources.jetbrains.com/help/img/idea/2025.3/docker_web_app_build_war.png)

### Pull the application server Docker image

  1. Open the [Services](services-tool-window.html) tool window: View | Tool Windows | Services or `Alt+8`.

  2. In the Services tool window, select the Images node, and then specify to pull the TomcatWildfly server image: `tomcat``jboss/wildfly`. Click Pull or press `Ctrl+Enter`.




You should see the `tomcat:latest``jboss/wildfly:latest` image in the list of images in the Services tool window.

### Run a Docker container application server and deploy your application to it

  1. In the Services tool window, right-click the `tomcat:latest``jboss/wildfly:latest` image and then click Create Container.

  2. In the Create Docker Configuration dialog, do the following:

     * Specify the name of the configuration: `TomcatConfig``WildflyConfig`

     * Specify the name of the container: `TomcatContainer``WildflyContainer`

     * Bind the container port 8080 to the host IP 127.0.0.1 and port 8080

     * Map the WAR artifact output directory [PROJECT_PATH]/target to the TomcatWildfly server deployment directory: /usr/local/tomcat/webapps/opt/jboss/wildfly/standalone/deployments.

![The Create Docker Configuration dialog](https://resources.jetbrains.com/help/img/idea/2025.3/docker_tutorial_deploy_java_web_app_in_tomcat.png)![The Create Docker Configuration dialog](https://resources.jetbrains.com/help/img/idea/2025.3/docker_tutorial_deploy_java_web_app_in_wildfly.png)

Click Run to start the container.

  3. When the container starts, open the following address in your web browser: <http://127.0.0.1:8080/DockerJavaWebApp-1.0-SNAPSHOT/>

You should see the following page:

![Simple Java Web App Demo start page](https://resources.jetbrains.com/help/img/idea/2025.3/DockerJavaWebApp-browser.png)



11 October 2024

[Run and debug a Spring Boot application using Docker Compose](run-and-debug-a-spring-boot-application-using-docker-compose.html)[Deploy and debug a Java web application inside a container running Tomcat](docker-tutorial-tomcat-debug.html)
