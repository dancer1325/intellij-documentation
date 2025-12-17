[//]: # (Source: https://www.jetbrains.com/help/idea/add-a-gradle-library-to-the-maven-repository.html)
[//]: # (Downloaded: 2025-12-17 19:17:43)

# Publish a Java library to a Maven repository

The purpose of this tutorial is to demonstrate how to publish a Java library created in the Gradle project to a local Maven repository and then to the remote one using IntelliJ IDEA.

Let's start with creating a Gradle project.

### Create a new Gradle project

  1. On the Welcome screen, select New Project. 

![Welcome Screen](https://resources.jetbrains.com/help/img/idea/2025.3/welcome_screen_gradle.png)

If your starting point is a project already opened in IntelliJ IDEA then go to File | New | Project in the main menu.

  2. On the page that opens, select Java from the list of options on the left. Enter the name for our project. In our case it is gradle-publish, select Gradle, leave the rest of the options as default, and click Create. 

![New Project dialog: select Gradle](https://resources.jetbrains.com/help/img/idea/2025.3/new_project_gradle.png)

IntelliJ IDEA creates a Gradle project and enables the Gradle tool window.




Now let's tweak the build.gradle file a little since we need to add support for a Java library and build our project.

### Edit build.gradle

  1. In the Project tool window, double-click the build.gradle file to open it in the editor. 

At this point build.gradle contains the following code:

plugins { id 'java' } group 'org.example' version '1.0-SNAPSHOT' repositories { mavenCentral() } dependencies { testImplementation platform('org.junit:junit-bom:5.10.0') testImplementation 'org.junit.jupiter:junit-jupiter' } test { useJUnitPlatform() } 

  2. In the `plugins` section, change `'java'` to `'java-library'`. 

plugins { id 'java-library' } group 'org.example' version '1.0-SNAPSHOT' repositories { mavenCentral() } dependencies { testImplementation platform('org.junit:junit-bom:5.10.0') testImplementation 'org.junit.jupiter:junit-jupiter' } test { useJUnitPlatform() } 

  3. Click ![the Sync Gradle Changes icon](https://resources.jetbrains.com/help/img/idea/2025.3/gradle.icons.gradleLoadChanges.svg) (Sync Gradle Changes) in the editor to synchronize the changes with your project.

  4. Use the src/main/java directory to add code for your library.

  5. Now in the Gradle tool window, click the project node, click Tasks, and then build.

  6. In the list that opens, double-click build to execute the build task that will generate our .jar file. 

![the Gradle tool window](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_build_task.png)

As a result, we have a generated .jar file located in the Project tool window, inside the build/libs directory.

![the Project tool window](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_publish_jar.png)



Now let us follow the Maven conventions and specify Maven coordinates for our library. Since IntelliJ IDEA has already added `GroupId` and `Version` when we created our project, the only thing that we need to change is `ArtifactId`.

### Change the ArtifactId and generate the JAR file

  1. In the Project tool window, double-click the settings.gradle file to open it in the editor. Change `rootProject.name` from `gradle-publish` to `my-artifact-id`. 

rootProject.name = 'my-artifact-id' 

  2. Click ![the Sync Gradle Changes icon](https://resources.jetbrains.com/help/img/idea/2025.3/gradle.icons.gradleLoadChanges.svg) Sync Gradle Changes to synchronize the changes.

  3. In the Gradle tool window, click Tasks.

  4. In the build directory first double-click the clean task to execute it and then execute the build task. 

IntelliJ IDEA will generate a .jar file with the information that is inline with the Maven naming conventions and the updated artifact name.

![the Project tool window](https://resources.jetbrains.com/help/img/idea/2025.3/my_artifact_jar.png)



Now let us work with our build script further and publish the library into a local Maven repository.

### Publish the library to a local Maven repository

  1. Open the build.gradle file and add `id 'maven-publish'` to the `plugins` section.

  2. Click ![the Sync Gradle Changes icon](https://resources.jetbrains.com/help/img/idea/2025.3/gradle.icons.gradleLoadChanges.svg) (Sync Gradle Changes) to synchronize the changes with your project.

  3. In the Gradle tool window, in the publishing section, double-click publishToMavenLocal to run the task.

![Run tool window / publishing result](https://resources.jetbrains.com/help/img/idea/2025.3/publish_task_result.png)

IntelliJ IDEA creates a JAR file and adds it, depending on your operating system, to the following directory:

/Users/<user_name>/.m2/[Artifact GroupID]/[Artifact Name]/[Artifact Version] 

/home/<user_name>/.m2/[Artifact GroupID]/[Artifact Name]/[Artifact Version]

C:\Users\<User_Name>\\.m2\\[Artifact GroupID]\\[Artifact Name]\\[Artifact Version]




We can edit the build.gradle file further to publish our library to the remote repository.

### Publish to the remote repository

  1. In the build.gradle file add the following section: 

publishing { publications { myLib(MavenPublication) { from components.java } } repositories { maven { name = "MyRepo" // optional target repository name url = "http://my.org.server/repo/url" credentials { username = 'alice' password = 'my-password' } } } } 

  2. Click ![the Sync Gradle Changes icon](https://resources.jetbrains.com/help/img/idea/2025.3/gradle.icons.gradleLoadChanges.svg) (Sync Gradle Changes) to load the changes to your project.

  3. In the Gradle tool window, open the publishing section and double-click publishAllPublicationsToMyRepository to run the task. 

![the Gradle tool window: publish task](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_tool_window_publish_task.png)



For more information about customizing the POM file, using a different snapshot, or releasing repositories, refer to [Gradle documentation](https://docs.gradle.org/current/userguide/publishing_maven.html).

23 April 2025

[Getting Started with Gradle](getting-started-with-gradle.html)[Set up JNI development in Gradle project](setting-up-jni-development-in-gradle-project.html)
