[//]: # (Source: https://www.jetbrains.com/help/idea/maven-refactorings.html)
[//]: # (Downloaded: 2025-12-17 19:32:10)

## Extract managed dependency

Let's say you have a multi-module project and in one of subprojects you have defined several dependencies that can be used by other subprojects.

You can use Extract managed dependency refactoring to extract such dependency into a parent POM under `dependencyManagement`.

  1. In your POM, select the dependency you want to extract. 

![POM with the dependency example](https://resources.jetbrains.com/help/img/idea/2025.3/maven_depen_extract.png)
  2. Press `Ctrl+Alt+M` or select Refactor | Extract | Extract Managed Dependency.

  3. IntelliJ IDEA extracts the selected dependency into a parent POM, automatically creating a `dependencyManagement` section and a full dependency definition. 

![parent POM with extracted dependency](https://resources.jetbrains.com/help/img/idea/2025.3/parent_pom_with_extraction.png)

Use gutter icons to see a popup with dependency descriptions or to navigate between parent and subprojects' dependencies.



