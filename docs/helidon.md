[//]: # (Source: https://www.jetbrains.com/help/idea/helidon.html)
[//]: # (Downloaded: 2025-12-17 19:28:41)

# Helidon

[Helidon](https://helidon.io/) is a Java framework for writing microservices. IntelliJ IDEA provides the following:

  * Coding assistance specific to both Helidon SE and Helidon MP

  * Integration with the [Endpoints](endpoints-tool-window.html) tool windows

  * A dedicated project creation wizard based on [start.microprofile.io](https://start.microprofile.io/)




### Create a new Helidon project

  1. In the main menu, go to File | New | Project.

  2. In the New Project wizard, select MicroProfile and choose the Default starter service [https://start.microprofile.io](https://start.microprofile.io/).

![New MicroProfile project wizard](https://resources.jetbrains.com/help/img/idea/2025.3/microprofile-new-project.png)

Click Next.

  3. Configure the following MicroProfile project settings:

     * Group: `com.example`

     * Artifact: `hello-helidon`

     * MicroProfile version: `MP32`

     * MicroProfile Runtime: `Helidon`

Click Next.

  4. Select the necessary specifications for your application and click Next.

  5. If necessary, change the project name, location, and other settings. Click Finish.




The generated project contains a REST endpoint named `HelloController` with the following code:

package com.example.hello.helidon; import javax.inject.Singleton; import javax.ws.rs.GET; import javax.ws.rs.Path; /** * */ @Path("/hello") @Singleton public class HelloController { @GET public String sayHello() { return "Hello World"; } } 

You can open the [Endpoints](endpoints-tool-window.html) tool window (View | Tool Windows | Endpoints) and see this endpoint:

![HelloController endpoint in the Endpoints tool window](https://resources.jetbrains.com/help/img/idea/2025.3/helidon-hello-endpoint.png)

### Run the Helidon application

  1. Open the `io.helidon.microprofile.server.Main` class from the Helidon library.

  2. In the gutter, click ![The Run icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.execute.svg) and run the `Main.main()` method `Ctrl+Shift+F10`.

  3. In the [Edit Configuration](run-debug-configuration.html) dialog, set Use classpath of module to your application's module: `hello-helidon`.

Click Run.




In the [Run tool window](run-tool-window.html), you will see that the server is running on `http://localhost:8080`. Open this URL in a web browser to see the landing page of the MicroProfile server.

The default root is located at `/data`, as defined by `@ApplicationPath("/data")` in the HellohelidonRestApplication class. Open `http://localhost:8080/data/hello` to see the output produced by the `HelloController` endpoint: `Hello World`.

17 June 2024

[GWT](gwt.html)[Vaadin](vaadin.html)
