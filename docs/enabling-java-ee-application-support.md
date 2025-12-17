[//]: # (Source: https://www.jetbrains.com/help/idea/enabling-java-ee-application-support.html)
[//]: # (Downloaded: 2025-12-17 19:25:44)

# Enterprise application support

By default, a Java Enterprise project in IntelliJ IDEA is not configured for full enterprise application development.

### Enable enterprise application support for your project

This information is valid for projects that are built with the native IntelliJ IDEA builder. If you're using a build tool, such as [Maven](maven-support.html) or [Gradle](gradle.html), make all changes using the build file.

  1. In the Project tool window `Alt+1`, select the necessary module.

  2. Press `Ctrl+Shift+A` and type `Add Framework Support`.

Once the action is found, click it to open the Add Framework Support dialog.

  3. In the dialog, select JavaEE Application and click OK.




This adds a deployment descriptor application.xml under META-INF in your project directory, a JavaEE Application facet and an enterprise application archive (EAR) artifact configuration.

### Manage deployment descriptors

A deployment descriptor describes how to deploy your application. It contains information about the configuration requirements, container options, and security settings. By default, IntelliJ IDEA generates one deployment descriptor for your enterprise application: META-INF/application.xml.

  1. Press `Ctrl+Alt+Shift+S` to open the Project Structure dialog.

  2. Open the Facets page and select the javaEEApplication facet.

You can click ![The Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) to add other deployment descriptors. You can also add deployment descriptors that are specific to your application server (runtime deployment descriptors).




### Manage application artifacts

Artifacts are the main application deliverables that you deploy to an application server.

  1. Press `Ctrl+Alt+Shift+S` to open the Project Structure dialog.

  2. Open the Artifacts page and select the default exploded EAR artifact configured for your application. You can see and configure the settings of this artifact or click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) to add a regular EAR archive artifact and create a manifest file for it.




You can build any of the configured artifacts by selecting Build | Build Artifacts from the main menu. You can also add these artifact configurations to your application server run configuration so that IntelliJ IDEA builds and deploys the artifacts as necessary.

### Migrate from Java EE to Jakarta EE

  1. In the main menu, go to Refactor | Migrate Packages and Classes.

  2. In the Package and Class Migration dialog, select the Java EE to Jakarta EE migration map and click Run.

If necessary, you can make a copy of the default migration map and adjust it to your needs. You can also select the module for which you want to perform the migration.




11 October 2024

[Tutorial: Your first Jakarta EE application](creating-and-running-your-first-jakarta-ee-application.html)[Contexts and Dependency Injection (CDI)](context-and-dependency-injection-cdi.html)
