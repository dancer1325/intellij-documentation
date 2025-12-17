[//]: # (Source: https://www.jetbrains.com/help/idea/netbeans.html)
[//]: # (Downloaded: 2025-12-17 19:32:58)

## Import a project to IntelliJ IDEA

  1. Launch IntelliJ IDEA.

If the [Welcome screen](run-for-the-first-time.html#start-project) opens, click Open.

Otherwise, go to File | Open in the main menu.

  2. In the dialog that opens, select the directory in which your sources, libraries, and other assets are located and click Open.

If you are using Maven with NetBeans, and you want to import a Maven project into IntelliJ IDEA, select your project's pom.xml.

  3. In the Open Project dialog that opens, click New Window.




IntelliJ IDEA will add the .idea directory to your project. This is used to store the IntelliJ IDEA [project settings](configure-project-settings.html) such as VCS settings, [inspection profiles](customizing-profiles.html), or [code styles](configuring-code-style.html). The NetBeans .nbproject directory and the build.xml file will remain untouched, and you'll be able to use IntelliJ IDEA along with NetBeans.

If you used NetBeans with Ant, keep in mind that the [Ant](ant.html) plugin is unbundled.

IntelliJ IDEA is fully integrated with Maven and Gradle. If you use one of these build tools, refer to [Maven](maven.html) and [Gradle](gradle.html) for more information about working with them in IntelliJ IDEA.
