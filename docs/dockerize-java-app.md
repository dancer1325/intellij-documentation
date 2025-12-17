[//]: # (Source: https://www.jetbrains.com/help/idea/dockerize-java-app.html)
[//]: # (Downloaded: 2025-12-17 19:25:18)

# Dockerize a Java application

You can use Docker to pack your compiled Java application into an image along with a specific runtime environment and any other necessary dependencies. You can then run a container from that image to see how the application will run in this environment. This is called dockerizing an application. 

This tutorial describes how to create a Dockerfile to build a Docker image with OpenJDK 17 and a compiled Java application. It also shows how to share this image with others and run a Docker container from it. 

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



By default, IntelliJ IDEA compiles the output to the HelloWorld.class file in the project directory under /out/production/DockerHelloWorld/, where `DockerHelloWorld` is the name of the current module.

### Create a Dockerfile

  1. In the Project tool window, right-click the project name, point to New and click File.

  2. In the New File dialog, type Dockerfile and press `Enter`.

  3. Paste the following code to the new Dockerfile:

FROM openjdk:17 COPY ./out/production/DockerHelloWorld/ /tmp WORKDIR /tmp ENTRYPOINT ["java","HelloWorld"] 




This Dockerfile contains instructions for building an image based on the `openjdk:17` image from [Docker Hub](https://hub.docker.com/). When you run a container from this image, Docker copies the contents of your project's output directory to the /tmp directory in the container (in this case, the output directory contains the main class HelloWorld.class). Then Docker sets the current working directory to /tmp and runs `java HelloWorld`. As a result, you should see `Hello, World!` printed to the container log.

### Build and run the image

  * In the gutter inside the Dockerfile, click ![The Run on Docker icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.runAll.svg) and select Run on 'Docker'.




IntelliJ IDEA creates a [Dockerfile run configuration](dockerfile-run-configuration.html), which builds an image from the Dockerfile and then runs a container based on that image. To see the whole process, open the Log tab in the Services tool window. 

![Docker log](https://resources.jetbrains.com/help/img/idea/2025.3/docker_new_project_dockerfile.png)

You can share the image with others, for example, to demonstrate exactly how your application is expected to run, without the need to install the necessary runtime (only Docker is required). 

To share built images, you need to [configure a Docker registry](docker-images.html#configure-registry) where you have permissions to push images. For example, you can create an account on [Docker Hub](https://hub.docker.com/) and share images using public or private repositories, or set up your own [Docker registry](https://docs.docker.com/registry/). 

### Share your Java application as a Docker image

  1. In the Services tool window, find the image that was built from the Dockerfile.

By default, it is designated by a unique image ID, because no image tag was provided when you created the image. You can edit the corresponding run configuration, specify an image tag of your choice, and run the configuration again.

To find the image, right-click the running container and select Image | Show Image.

![Show image that was used to run the Docker container](https://resources.jetbrains.com/help/img/idea/2025.3/docker_tutorial_run_java_share_image.png)
  2. Right-click the image with the required ID and then click Push Image in the context menu.

  3. In the Push Image dialog, select your registry, specify the repository name and tag for the image, and click OK.




Once Docker pushed the image to the registry, anyone with access to it can pull it and run a container from this image. You can be sure that they will run the exact version of your application on the specific runtime version that you've set in the Dockerfile.

25 September 2025

[Run a database in a Docker container](running-a-dbms-image.html)[Run and debug a Java application with Docker](running-a-java-app-in-a-container.html)
