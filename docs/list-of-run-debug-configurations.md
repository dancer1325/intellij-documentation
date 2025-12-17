[//]: # (Source: https://www.jetbrains.com/help/idea/list-of-run-debug-configurations.html)
[//]: # (Downloaded: 2025-12-17 19:31:30)

# List of run/debug configuration templates

This page lists [run/debug configuration](run-debug-configuration.html) templates available in IntelliJ IDEA. For more information about using them in your project, refer to the related how-to pages.

Whether a run/debug configuration is available in your IDE may depend on which [plugins](managing-plugins.html) are installed and enabled.

This page only covers the standard set of run/debug configurations for IntelliJ IDEA Community and Ultimate, and some of the non-bundled JVM plugins. For other languages, like JavaScript, see the documentation for the related products (for example, WebStorm). Third-party and non-bundled plugins are out-of-scope for this documentation.

Name| Use it to| Required plugins  
---|---|---  
[Ammonite](run-debug-configuration-ammonite.html)| Run Scala scripts using [Ammonite](http://ammonite.io/#Ammonite-REPL), which is a modernized version of Scala REPL. For more information, refer to the [Ammonite](work-with-scala-worksheet-and-ammonite.html) section.| Scala  
[Application](run-debug-configuration-java-application.html)| Compile your Java application with `javac` and run it with `java`.|   
[Attach to Node.js/Chrome](run-debug-configuration-node-js-remote-debug.html) (Ultimate) | Attach to and debug already running [Node.js](http://nodejs.org/) applications.| Node.js  
[Compound](run-debug-multiple.html#compound-configs)| Run several run/debug configurations in parallel. This is useful, for example, if you want to launch various automated tests or client-server apps. The controls for each configuration will be available in a separate tab in the Run or Debug tool window.|   
[Dockerfile](dockerfile-run-configuration.html)| Created automatically when you [run a container from a Dockerfile](docker-containers.html#run_image_dockerfile). This configuration builds an image from the Dockerfile, and then derives a container from this image.| Docker  
[Docker Image](docker-image-run-configuration.html)| Created automatically when you [run a container from an existing image](docker-containers.html#run_image). You can run it from a locally existing Docker image that you either [pulled](docker-images.html#pull-image) or [built](docker-images.html#build-image) previously.| Docker  
[Docker Compose](docker-compose-run-configuration.html)| Created automatically when you [run a multi-container Docker application](docker-compose.html) from a [Docker Compose file](https://docs.docker.com/compose/overview/).| Docker  
[Gradle](create-run-debug-configuration-gradle-tasks.html)| Run Gradle tasks.| Gradle  
[Groovy](run-debug-configuration-groovy.html)| Run and debug Groovy scripts. For more information, refer to the [Groovy](getting-started-with-groovy.html#run_groovy) section.| Groovy  
[Grunt.js](run-debug-configuration-grunt.html)| Run and debug Grunt.js tasks.|   
[Gulp.js](run-debug-configuration-gulp-js.html)| Run and debug Gulp.js tasks.|   
[HTTP Request](http-client-in-product-code-editor.html#http-request-run-debug-configurations) (Ultimate) | Execute HTTP Requests directly in the IntelliJ IDEA either individually or as part of a compound run/debug configuration.| HTTP Client  
[JAR](run-debug-configuration-jar.html)| Run and debug applications started via `java -jar<name>.jar` command. IntelliJ IDEA does not build the JAR by default. To include the build process as a step, add a Before Launch task.Tutorial: [Create your first Java application](creating-and-running-your-first-java-application.html).|   
[Java Scratch](run-debug-configuration-java-scratch.html)| Run and debug Java [scratch files](scratches.html) that have the `main()` method defined.|   
[JavaScript Debug](run-debug-configuration-javascript-debug.html)| Debug JavaScript in applications running on the built-in or on an external web server and to debug Dart web applications.| JavaScript Debugger  
[Jest](run-debug-configuration-jest.html) (Ultimate) | Run and debug [Jest](https://facebook.github.io/jest/) tests.|   
[JUnit](run-debug-configuration-junit.html)| Configure and run unit tests based on the JUnit testing framework.| JUnit  
[Karma](run-debug-configuration-karma.html) (Ultimate) | Run and debug JavaScript unit tests using the [Karma test runner](http://karma-runner.github.io/0.12/index.html).| Karma  
[Kotlin](run-debug-configuration-kotlin.html)| Run and debug Kotlin applications.| Kotlin  
[Kotlin Script](run-debug-configuration-kotlin-script.html)| Run and debug Kotlin scripts.| Kotlin  
[Maven](run-debug-configuration-maven.html)| Build and launch Maven projects| Maven  
[Mocha](run-debug-configuration-mocha.html) (Ultimate) | Run and debug JavaScript unit tests using the [Mocha test framework](http://mochajs.org).| Node.js  
[Node.js](run-debug-configuration-node-js.html) (Ultimate) | Debug Node.js applications.| Node.js  
[Nodeunit](run-debug-configuration-nodeunit.html) (Ultimate) | Run and debug unit tests for Node.js applications| Node.js  
[NPM](run-debug-configuration-npm.html)| Run and debug [npm](https://docs.npmjs.com/misc/scripts) and [Yarn](https://yarnpkg.com/en/) scripts locally, that is when IntelliJ IDEA itself starts Node.js installed on your computer and initiates script execution.|   
[Plugin](run-debug-configuration-plugin.html)| Run or debug plugin projects.|   
[Protractor](run-debug-configuration-protractor.html) (Ultimate) | Run and debug AngularJS unit tests using the Protractor test runner.|   
[React Native](react-native.html#ws_react_native_create_run_config) (Ultimate) | Run and debug [React Native](http://www.reactnative.com/) applications.|   
[Remote JVM Debug](attach-to-process.html#create-rc)| Attach to a remote JVM or listen for incoming connections over a socket or shared memory (Windows). This run/debug configuration represents the debugger end. The host application has to be started separately. For detailed procedures, refer to [Attach to process](attach-to-process.html) and [Tutorial: Remote debug](tutorial-remote-debug.html).|   
[Scala REPL](run-debug-configuration-scala-repl.html)| Evaluate Scala expressions in the Run tool window. However, the preferred way to invoke [Scala REPL](https://docs.scala-lang.org/overviews/repl/overview.html) is to select Tools | Scala REPL from the main menu. In this case, the run/debug configuration is created automatically, and you can modify it as needed.| Scala  
[TestNG](run-debug-configuration-testng.html)| Launch tests that comply with the TestNG framework.| TestNG  
[ScalaTest](run-debug-configuration-scala-test.html)| Run Scala tests and test scopes with [ScalaTest](https://www.scalatest.org/), which is the most flexible and most popular testing tool in the Scala ecosystem. For more information, refer to the [Scala testing](run-debug-and-test-scala.html#test_scala_app) section.| Scala  
[Specs2](run-debug-configuration-specs2.html)| Run Scala test specifications. For more information, refer to the [Scala testing](run-debug-and-test-scala.html#test_scala_app) section.| Scala  
[Spring Boot](run-debug-configuration-spring-boot.html) (Ultimate)| Run Spring Boot applications. For more information, refer to [Spring Boot](spring-boot.html).| Spring, Spring Boot  
[Tomcat Server](run-debug-configuration-tomcat-server.html) (Ultimate)| Deploy and debug your applications on [Apache Tomcat](http://tomcat.apache.org).| Tomcat and TomEE  
[TomEE](run-debug-configuration-tomee.html) (Ultimate)| Deploy and debug your applications on [Apache TomEE](http://tomee.apache.org).| Tomcat and TomEE  
[XSLT](run-debug-configuration-xslt.html)| Run XSLT scripts.| XPathView + XSLT  
  
03 September 2025

[Program arguments, VM options, environment variables](program-arguments-and-environment-variables.html)[Tutorial: Run a Java application](run-java-applications.html)
