[//]: # (Source: https://www.jetbrains.com/help/idea/tms-annotations-setup.html)
[//]: # (Downloaded: 2025-12-17 20:04:25)

# TMS link annotations

Annotations are special markers in code that contain metadata about code. You can use TMS link annotations to provide additional information about tests. This allows IntelliJ IDEA to link your unit tests to TMS items.

TMS link annotations enable IntelliJ IDEA to perform better analysis, for example, to find test cases that are already referenced from unit tests.

An annotation is just a class with a declaration similar to the following:

@interface MyAnnotation { } // Java annotation class MyAnnotation // Kotlin 

Your project may already use an annotation that links code to the corresponding tests. If that is the case, you can proceed with [configuring IntelliJ IDEA to recognize this annotation.](#configure-settings)

If not, you can [use a third-party annotation](#use-third-party-annotation) or [create your own custom annotation](#create-custom-annotation). Both options work equally well.

### Import a third-party annotation

  1. Open pom.xml in the root directory of your project.

To quickly navigate to a file, press `Ctrl+Shift+N` and enter its name.

  2. In pom.xml, press `Alt+Insert`, and select Dependency. 

![Generate a dependency](https://resources.jetbrains.com/help/img/idea/2025.3/aqua_tms_generate_annotation_maven.png)
  3. In the tool window that opens, enter the name of the dependency, for example, `io.qameta.allure:allure-java-commons`.

Make sure to select the required dependency version and click Add.

![Selecting dependency](https://resources.jetbrains.com/help/img/idea/2025.3/aqua_tms_import_annotation.png)
  4. Apply the changes in the build script. For that, press `Ctrl+Shift+O` or click Sync Maven Changes in the notification that appears in the top-right corner of the editor.

![Loading changes](https://resources.jetbrains.com/help/img/idea/2025.3/aqua_tms_import_annotation_reload_maven.png)



### Import a third-party annotation

  1. Open build.gradle in the root directory of your project.

To quickly navigate to a file, press `Ctrl+Shift+N` and enter its name.

  2. In build.gradle, press `Alt+Insert`, and select Add Maven artifact dependency. 

![Generate a dependency](https://resources.jetbrains.com/help/img/idea/2025.3/aqua_tms_generate_annotation_gradle.png)
  3. In the tool window that opens, enter the name of the dependency, for example, `io.qameta.allure:allure-java-commons`.

Make sure to select the required dependency version and click Add.

![Selecting dependency](https://resources.jetbrains.com/help/img/idea/2025.3/aqua_tms_import_annotation.png)
  4. Apply the changes in the build script. For that, press `Ctrl+Shift+O` or click Sync Gradle Changes in the notification that appears in the top-right corner of the editor.

![Loading changes](https://resources.jetbrains.com/help/img/idea/2025.3/aqua_tms_import_annotation_reload_gradle.png)



If you cannot add extra dependencies to your module, you can create your own annotation class.

### Create a custom annotation

  1. In the Project tool window (`Alt+1`), right-click the node in which you want to create a new class and select New | Java Class.

  2. Paste the code below to the file. You can replace `MyTmsAnnotation` with any other valid name.

public @interface MyTmsAnnotation { public String value() default ""; } 




### Create a custom annotation

  1. In the Project tool window (`Alt+1`), right-click the node in which you want to create a new class and select New | Kotlin Class/File.

  2. Paste the code below to the file. You can replace `MyTmsAnnotation` with any other valid name.

annotation class MyTmsAnnotation(val value: String = "") 




After the annotation is already in the project, you need to tell the TMS plugin to use that specific annotation.

### Enable annotations in TMS settings

  1. Press `Ctrl+Alt+S` to open settings and then select Tools | TMS | References From Code | Java/Kotlin.

  2. Click Add ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) to add the annotation.

![TMS settings](https://resources.jetbrains.com/help/img/idea/2025.3/aqua_tms_settings.png)
  3. Specify the annotation class and click OK.

![Enable annotations in settings](https://resources.jetbrains.com/help/img/idea/2025.3/aqua_tms_setup_annotation.png)



Finally, for IntelliJ IDEA to establish a linkage between a unit test and a TMS item, the test needs to be annotated with one of the annotations configured for the project.

### Annotate a unit test

  1. Open the unit test file in the editor.

  2. Put a TMS link annotation before the method definition as shown below.

// C58439 @MyTmsAnnotation("C58439") @Test void TestCase1() { Assertions.assertEquals(4, Calculator.multiply(2,2)); } 




### Annotate a unit test

  1. Open the unit test file in the editor.

  2. Put a TMS link annotation before the method definition as shown below.

// C58439 @MyTmsAnnotation("C58439") @Test fun TestCase1() { Assertions.assertEquals(4, Calculator.multiply(2,2)) } 




24 October 2024

[Get started with TMS integration](test-management-systems.html)[Local TMS](local-tms.html)
