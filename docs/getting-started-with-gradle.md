[//]: # (Source: https://www.jetbrains.com/help/idea/getting-started-with-gradle.html)
[//]: # (Downloaded: 2025-12-17 19:27:57)

## Step 1. Create a project

Let's create a Gradle project with Java.

### Create a new Gradle Project with IntelliJ IDEA

  1. On the welcome screen, click New Project.

![New project Gradle](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_project_wizard_start.png)
  2. On the page that opens, let's specify our project's name (FizzBuzz) and the location.

  3. Let's select the Java option, which is what we need for our project and Gradle since we are creating a Gradle project.

  4. IntelliJ IDEA automatically adds a project SDK (JDK) in the JDK field. In our tutorial, we use the open JDK 14 version.

You can change the selected JDK, IntelliJ IDEA will download the appropriate Gradle version. The only thing you need to have is the internet connection.

Let's leave the default Groovy for Gradle DSL and unselect the Add sample code option since we're going to add our own code from scratch.

  5. We can use the default information for ArtifactId which basically is the name of our project and leave the default information in the GroupId field.

Click Create.




After we've created our project, and it finished indexing, let's see what is inside:

  * IntelliJ IDEA creates a project with the build.gradle file including the following code:

plugins { id 'java' } group 'org.example' version '1.0-SNAPSHOT' repositories { mavenCentral() } dependencies { testImplementation 'org.junit.jupiter:junit-jupiter-api:5.10.0' testImplementation 'org.junit.jupiter:junit-jupiter' } test { useJUnitPlatform() } 

As you can see, IntelliJ IDEA conveniently adds a test dependency. IntelliJ IDEA supports code completion inside the build.gradle file. So, if we decide to add more dependencies, IntelliJ IDEA will quickly locate their names and versions.

  * IntelliJ IDEA also creates the src folder with main and test subdirectories in the Project tool window. 

![Gradle project view](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_project_view.png)
  * IntelliJ IDEA enables the dedicated Gradle tool window with a liked project and its default tasks. We will use this window to run our tasks. 

![Gradle tool window](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_tool_window.png)

If you closed this window, you can always access it from the main menu by selecting View | Tool Windows | Gradle.

  * The [Gradle settings](gradle-settings.html) in our project are used to store the information about the linked projects, Gradle JVM, and build actions. You can quickly access them from the Gradle tool window (click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) on the toolbar). 

![the Gradle settings](https://resources.jetbrains.com/help/img/idea/2025.3/gradle_settings_FizzBuzz.png)

As you can see, the build and test actions are delegated to Gradle. Also, the Gradle wrapper was used to determine Gradle for our project.

  * The [project structure](project-settings-and-structure.html) (`Ctrl+Alt+Shift+S`) contains information about the project's JDK and a language level used in the project. 

![Project Structure](https://resources.jetbrains.com/help/img/idea/2025.3/project_structure_FizzBuzz.png)


