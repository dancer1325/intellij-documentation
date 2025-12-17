[//]: # (Source: https://www.jetbrains.com/help/idea/run-debug-configuration-junit.html)
[//]: # (Downloaded: 2025-12-17 19:58:19)

## Required options

Item| Description  
---|---  
JRE| Specify the runtime environment that IntelliJ IDEA should use to run the application. By default, IntelliJ IDEA uses the latest available JDK from the module dependencies.  
Use classpath of module| Select the module whose classpath should be used to run the application.  
Test kind| From this list, select the scope for your tests and fill in the fields depending on your selection:

  * All in package: run all unit tests in a package. Specify the package in the field to the right.
  * All in directory: run all unit tests in a directory. Specify the directory in the field to the right.
  * Pattern: run a set of test classes or specific methods within test classes. This set may include classes located in the same or different directories, packages, or modules. Declarations must be separated with `||`.Each class in this field must be represented by its fully qualified name:
    * Include the package name and class name
    * Use `,` as a separator for methods
    * Use `$` as a separator for inner classes
You can type class names manually, or click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.open.svg) on the right (or press `Shift+Enter`) and search for classes you want to add in the dialog that opens.Example: `packageName.ClassName$InnerClassName,methodName`You may also specify the required classes using [regular expressions](regular-expressions.html).For example, if you want to exclude all integration tests that have `IT` in their names, type `^(?!.*IT.*).*$`.You can create a suite test, that is, a bundle of several test classes that will be run together. To create a suite test class, click ![the Expand button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.expandComponent.svg) on the right and type the test classes you want to be run as a suite. As a result, a new class will be created with the `@Suite` annotation.
  * Class: run all unit tests in a class. Specify the fully qualified name of the class in the field to the right.
  * Method: run an individual test method. Specify the fully qualified name of the class with this method and the method name in the field to the right.
  * Category: run all tests in a [category](https://junit.org/junit4/javadoc/4.12/org/junit/experimental/categories/Categories.html). Specify the category in the field to the right.
  * UniqueId: include tests and containers with a specific ID in the testing scope. Specify the ID in the field to the right.
  * Tags: (JUnit 5) run classes and methods tagged with the `@Tag` annotation in the testing scope.Tag expressions are boolean expressions with the following allowed operators: `!` (not), `&` (and), and `|` (or). Parentheses can be used to adjust for operator precedence. For more information and examples, refer the [JUnit 5 documentation](https://junit.org/junit5/docs/5.3.0/api/org/junit/platform/launcher/TagFilter.html).

  
Working directory| Specify the working directory to be used for running the application. This directory is the starting point for all relative input and output paths. By default, the working directory is the project root.
