[//]: # (Source: https://www.jetbrains.com/help/idea/thymeleaf.html)
[//]: # (Downloaded: 2025-12-17 20:04:24)

## Add Thymeleaf support

You can add Thymeleaf support when creating a project or module, or for an existing project or module. IntelliJ IDEA downloads the selected Thymeleaf library files and adds them to the dependencies of the corresponding module.

You can also create a Thymeleaf project by opening an appropriate pom.xml file. In this case, Maven will manage the dependencies in your project. For more information, refer to [Maven](maven-support.html).

### New Java Enterprise project or module with Thymeleaf

  1. In the main menu, go to File | New | Project or File | New | Module.

  2. In the dialog that opens, select Jakarta EE from the list on the left and click Next.

  3. In the Dependencies list, under Implementations, select Thymeleaf, and click Next.

  4. Enter a name for your project or module and click Finish.




For more information about Java Enterprise projects, refer to [Tutorial: Your first Jakarta EE application](creating-and-running-your-first-jakarta-ee-application.html).

### New Spring project or module with Thymeleaf

  1. Go to File | New | Project or File | New | Module.

  2. In the dialog that opens, select Spring Initializr from the list on the left and click Next.

  3. From the Dependencies list, click Template Engines and select the Thymeleaf option. 

![Add Thymeleaf](https://resources.jetbrains.com/help/img/idea/2025.3/add_thymeleaf_new_project.png)
  4. Click Create.




For more information about Spring projects, refer to [Tutorial: Create your first Spring application](your-first-spring-application.html).

### Enable Thymeleaf support for an existing project

  1. Open the build file in the editor (pom.xml or build.gradle depending on the build tool that you use in your project).

  2. Add the following dependency, but make sure to change the version according to your project's requirements:

<dependency> <groupId>org.thymeleaf</groupId> <artifactId>thymeleaf</artifactId> <version>3.0.12.RELEASE</version> </dependency>

implementation('org.thymeleaf:thymeleaf:3.0.12.RELEASE') 

  3. Press `Ctrl+Shift+O` to import the changes.




For more information about working with build tools, refer to [Maven](maven-support.html) or [Gradle](gradle.html).

### Thymeleaf support features

Support for [Thymeleaf](https://www.thymeleaf.org/) in IntelliJ IDEA includes the following:

Code completion
    

[Code completion](auto-completing-code.html) for expressions and `th:*` attributes.

Navigation from a reference
    

Navigation from a reference in a template to the corresponding getter method, message in a .properties file, or another appropriate code fragment. Go to Navigate | Declaration or Usages or press `Ctrl+B`.

Navigation to type definitions
    

Go to Navigate | Type Declaration or press `Ctrl+Shift+B`.

Refactorings
    

The Rename refactoring for referenced properties, getter methods, iteration and status variables, and so on. Go to Refactor | Rename or press `Shift+F6`.

Inspections
    

[Code inspections](code-inspection.html) that help you find and fix unresolved references and errors in expression syntax.

Intention actions
    

[Intention actions](intention-actions.html), such as Create property for unresolved message references or Import class for adding the `import` statements to `org.thymeleaf.*` classes.

Prototypes preview
    

[Preview of your prototypes](#preview-feature-with-thymeleaf) (the static part of your templates) in a web browser from the editor.
