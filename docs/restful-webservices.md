[//]: # (Source: https://www.jetbrains.com/help/idea/restful-webservices.html)
[//]: # (Downloaded: 2025-12-17 19:57:46)

# RESTful web services

IntelliJ IDEA provides support for developing, debugging, and testing of Java web services that comply to the representational state transfer (REST) architectural pattern. This includes various assistance features for the following:

  * [Jakarta RESTful Web Services](https://jakarta.ee/specifications/restful-ws/) API

  * [Eclipse Jersey](https://eclipse-ee4j.github.io/jersey/) framework




Since REST is an architectural pattern, there is no definite workflow to develop RESTful web services. This section outlines some common approaches to developing REST applications in IntelliJ IDEA.

### Developing RESTful web services

  1. Make sure to enable the Jakarta EE: RESTful Web Services (JAX-RS) bundled plugin and either create a new Jakarta EE project or module, or enable the RESTful web services development support for an existing module. For more information, refer to [Get started with REST development](preparing-for-rest-development.html). 

  2. Create the necessary classes and methods in the RESTful web service module.

  3. Configure the [artifacts](working-with-artifacts.html) to deploy.

  4. [Create a run configuration](run-debug-configuration.html#createExplicitly). On the Deployment tab, specify the artifacts to deploy.

  5. Deploy the web service to an HTTP server and start the server.

  6. [Run](running-applications.html) the application locally or on a remote host.

  7. Test the RESTful web service using the [built-in HTTP client](http-client-in-product-code-editor.html).




11 October 2024

[Getting started with Google App Engine](getting-started-with-google-app-engine.html)[Tutorial: Your first RESTful web service](creating-and-running-your-first-restful-web-service.html)
