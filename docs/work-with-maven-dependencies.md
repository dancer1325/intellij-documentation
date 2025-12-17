[//]: # (Source: https://www.jetbrains.com/help/idea/work-with-maven-dependencies.html)
[//]: # (Downloaded: 2025-12-17 20:07:08)

## Add a Maven dependency

IntelliJ IDEA lets you add a Maven dependency to your project. We recommend that you specify the dependency inside your POM. Dependencies that you set up manually inside IntelliJ IDEA [module settings](creating-and-managing-modules.html) will be discarded on the next Maven project reload.

  1. Open your POM in the editor.

  2. Press `Alt+Insert` to open the Generate context menu.

  3. From the context menu, select Dependency.

  4. In the Maven Artifact Search tool window, in the search field, start typing the name of your dependency. In the list of results select the one you need and click Add.

![Maven Artifact Search](https://resources.jetbrains.com/help/img/idea/2025.3/maven_artifact_search.png)

IntelliJ IDEA adds the dependency to your pom.xml.

![the Maven Tool Window](https://resources.jetbrains.com/help/img/idea/2025.3/mvn_dependencies_tool_window.png)

IntelliJ IDEA also adds the dependency to the Dependencies node in the Maven tool window and to the External Libraries in the Project tool window.

If the added dependency has its own transitive dependencies, IntelliJ IDEA displays them in both tool windows.

![the Maven tool window](https://resources.jetbrains.com/help/img/idea/2025.3/maven_dependency_trans.png)



### Enable annotation processors

  1. Open your POM file.

  2. Specify the `annotationProcessors` and `annotationProcessorPaths` options. 

For example, check the following code:

<build> <plugins> <plugin> <groupId>org.apache.maven.plugins</groupId> <artifactId>maven-compiler-plugin</artifactId> <version>3.5.1</version> <configuration> <annotationProcessorPaths> <path> <groupId>org.sample</groupId> <artifactId>sample-annotation-processor</artifactId> <version>1.2.3</version> </path> </annotationProcessorPaths> </configuration> </plugin> </plugins> </build>

For more information, refer to [Maven](https://maven.apache.org/plugins/maven-compiler-plugin/compile-mojo.html).

  3. Re-import your project. IntelliJ IDEA creates an annotation processors profile, enables the annotation processing and adds the appropriate path to the [Annotation Processor](annotation-processors-support.html#annotation_processing) settings located in Settings | Build, Execution, Deployment | Compiler. 

![Annotation processors settings](https://resources.jetbrains.com/help/img/idea/2025.3/annotationProcessorsMaven.png)


