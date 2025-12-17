[//]: # (Source: https://www.jetbrains.com/help/idea/maven-tab.html)
[//]: # (Downloaded: 2025-12-17 19:32:15)

# Maven tab

File | Project Structure | Artifacts | <artifact> | Maven

Use this tab to specify settings for Maven projects with WAR artifacts.

![the Maven tab](https://resources.jetbrains.com/help/img/idea/2025.3/maven_tab.png)

Item| Description  
---|---  
Unpack nested archives| Select this option if you want IntelliJ IDEA to unpack nested JAR files. For [example](#example), you have a multi-module Maven project where a module depends on the other one and has an EAR or WAR artifact. In this case, when you import or deploy such module, IntelliJ IDEA creates a JAR file with module dependencies. If you want a dependency to such module be deployed as a folder instead of a JAR file, select this option.Don't forget to re-import your changes. IntelliJ IDEA will remind you to do so with the appropriate popup.  
Show content of elements| Select this option if you want the contents of certain elements to be displayed in the layout tree. Click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) to select the needed elements:

  * Show Library Files
  * Show Content of Included Artifacts
  * Show Content of JavaEE Facets
  * Show Content of JPA Resources

  
  
![JAR files with dependencies](https://resources.jetbrains.com/help/img/idea/2025.3/ear_exploded_jar.png)

![Unpacked into directories](https://resources.jetbrains.com/help/img/idea/2025.3/ear_exploded_directory.png)

28 June 2024

[Validation tab](validation-tab.html)[Java FX tab](project-structure-artifacts-java-fx-tab.html)
