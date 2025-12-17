[//]: # (Source: https://www.jetbrains.com/help/idea/work-with-maven-profiles.html)
[//]: # (Downloaded: 2025-12-17 20:07:11)

## Declare Maven profiles

IntelliJ IDEA lets you declare profiles explicitly in the POM of your project. Using code completion, you can place a number of different configurations inside the `profiles` tags and override the default configurations specified in your POM for Maven plugins, dependencies, repositories, and so on.

  1. Open your POM in the editor.

  2. Specify the `<profiles>` section and declare the profiles. 

![Profile declaration](https://resources.jetbrains.com/help/img/idea/2025.3/maven_profile_declaration.png)

IntelliJ IDEA displays them in the Profiles list of the Maven tool window. 

![Maven tool window](https://resources.jetbrains.com/help/img/idea/2025.3/maven_tool_win_declared_profiles.png)



Alternatively, you can declare profiles using one of the following ways:

  * You can define them locally in the Maven settings directory %USER_HOME%/.m2/settings.xml.

  * You can define them globally in the global Maven settings ${maven.home}/conf/settings.xml.

  * You can define them in the profile descriptor located in the project's base directory (profiles.xml). Note that this option is not supported in Maven 3. See [Maven 3 compatibility notes](https://cwiki.apache.org/confluence/display/MAVEN/Maven+3.x+Compatibility+Notes).



