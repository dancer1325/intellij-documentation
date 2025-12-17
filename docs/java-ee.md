[//]: # (Source: https://www.jetbrains.com/help/idea/java-ee.html)
[//]: # (Downloaded: 2025-12-17 19:30:14)

# Jakarta EE

IntelliJ IDEA provides [support for developing](https://www.jetbrains.com/idea/jakarta/) enterprise Java applications based on [Jakarta EE](https://jakarta.ee/) (formerly known as Java EE). All the required plugins are bundled and enabled by default in IntelliJ IDEA Ultimate. The main plugin is Jakarta EE Platform for the core platform support, such as a dedicated project wizard. Other plugins that start with Jakarta EE in their name add support for various specifications, such as JPA, JAX-RS, and so on.

Jakarta EE support is limited in IntelliJ IDEA without the Ultimate subscription.

Depending on the set of plugins that you have enabled, IntelliJ IDEA does a lot of routine setup work for you. For example, it can create the relevant [facet](adding-support-for-frameworks-and-technologies.html) in your project, generate and update deployment descriptors and manifest files according to your project settings, add artifact configurations (JAR, WAR, EAR), detect problems and errors with how your application is configured. You can use dedicated [run configurations](run-debug-configuration.html) for most of the supported application servers to start the corresponding server if necessary, build and deploy your artifacts, and open a predefined URL in your web browser. This greatly reduces the amount of manual setup and routine actions.

IntelliJ IDEA supports Jakarta EE up to version 11. In terms of functionality, Jakarta EE 9 is essentially the same as Jakarta EE 8 (fully compatible with Java EE 8), with the difference being in internal naming: the API namespace was renamed from `javax` to `jakarta`. So all features in IntelliJ IDEA that provide Java EE support also apply to Jakarta EE.

In IntelliJ IDEA 2022.1, all Java EE plugins were renamed `Jakarta EE`. For example, the Java EE Platform plugin is now called Jakarta EE Platform.

If you are new to enterprise Java development, start with [Tutorial: Your first Jakarta EE application](creating-and-running-your-first-jakarta-ee-application.html). Then you can read more about the supported [application servers](application-servers-support.html) and [cloud providers](working-with-clouds.html). And learn how to develop your own [RESTful web service](restful-webservices.html).

Here is a video to get you started:

26 November 2025

[JVM frameworks](jvm-frameworks.html)[Tutorial: Your first Jakarta EE application](creating-and-running-your-first-jakarta-ee-application.html)
