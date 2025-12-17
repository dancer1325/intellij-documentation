[//]: # (Source: https://www.jetbrains.com/help/idea/junit.html)
[//]: # (Downloaded: 2025-12-17 19:30:49)

# Get started with JUnit

In this tutorial, you will learn how to set up JUnit for your projects, create tests, and run them to see if your code is operating correctly. It contains just the basic steps to get you started.

If you want to know more about JUnit, refer to [the official documentation](https://junit.org/junit5/). To learn more about testing features of IntelliJ IDEA, refer to other topics in this section. 

You can choose to follow the tutorial using either Maven, Gradle, or the IntelliJ builder.

### Create a project

  1. In the main menu, go to File | New | Project.

  2. In the New Project wizard, select Java from the list on the left.

  3. Specify the name for the project, for example, `junit-tutorial`, and select Maven as a build tool.

  4. From the JDK list, select the [JDK](sdk.html#jdk) that you want to use in your project.

If the JDK is installed on your computer, but not defined in the IDE, select Add JDK and specify the path to the JDK home directory.

If you don't have the necessary JDK on your computer, select Download JDK.

  5. Click Create.




For more information about working with Maven projects, refer to [Maven](maven-support.html).

### Add dependencies

For our project to use JUnit features, we need to add JUnit as a dependency.

  1. Open pom.xml in the root directory of your project.

To quickly navigate to a file, press `Ctrl+Shift+N` and enter its name.

  2. In pom.xml, press `Alt+Insert` and select Dependency.

  3. In the dialog that opens, type `org.junit.jupiter:junit-jupiter` in the search field.

Locate the necessary dependency in the search results and click Add.

  4. When the dependency is added to pom.xml, press `Ctrl+Shift+O` or click ![Reimport All Maven Projects](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.refresh.svg) in the Maven tool window to import the changes. 

![The Sync Maven Changes button](https://resources.jetbrains.com/help/img/idea/2025.3/junit-tutorial-maven-reload.png)



In the result of adding the dependency, your pom.xml file will look similar to this:

<?xml version="1.0" encoding="UTF-8"?> <project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd"> <modelVersion>4.0.0</modelVersion> <groupId>org.example</groupId> <artifactId>junit-tutorial</artifactId> <version>1.0-SNAPSHOT</version> <properties> <maven.compiler.source>21</maven.compiler.source> <maven.compiler.target>21</maven.compiler.target> <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding> </properties> <dependencies> <dependency> <groupId>org.junit.jupiter</groupId> <artifactId>junit-jupiter-engine</artifactId> <version>5.7.0</version> </dependency> </dependencies> </project>

The procedure above shows the manual way so that you know what happens behind the scenes and where you set up the testing framework. However, if you just start writing tests, IntelliJ IDEA [will automatically detect if the dependency is missing and prompt you to add it](testing.html#add-testing-libraries).

### Write application code

Let's add some code that we'll be testing.

  1. In the Project tool window `Alt+1`, right-click the src/main/java folder and select New | Java Class. Name the class `Calculator.java`.

  2. Paste the following code in the file: 

import java.util.stream.DoubleStream; public class Calculator { static double add(double... operands) { return DoubleStream.of(operands) .sum(); } static double multiply(double... operands) { return DoubleStream.of(operands) .reduce(1, (a, b) -> a * b); } } 




### Create a project

  1. In the main menu, go to File | New | Project.

  2. In the New Project wizard, select Java from the list on the left.

  3. Specify the name for the project, for example, `junit-tutorial`, and select Gradle as a build tool.

  4. From the JDK list, select the [JDK](sdk.html#jdk) that you want to use in your project.

If the JDK is installed on your computer, but not defined in the IDE, select Add JDK and specify the path to the JDK home directory.

If you don't have the necessary JDK on your computer, select Download JDK.

  5. Click Create.




For more information about working with Gradle projects, refer to [Gradle](gradle.html).

### Add dependencies

Newly created Gradle projects usually have the latest JUnit dependency by default. If it is missing, you can add JUnit as a dependency manually.

  1. Open build.gradle in the root directory of your project.

To quickly navigate to a file, press `Ctrl+Shift+N` and enter its name.

  2. In build.gradle, press `Alt+Insert` and select Add Maven artifact dependency.

  3. In the tool window that opens, type `org.junit.jupiter:junit-jupiter` in the search field.

Locate the necessary dependency in the search results and click Add.

  4. When the dependency is added to build.gradle, press `Ctrl+Shift+O` or click ![Reimport All Gradle Projects](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.refresh.svg) in the Gradle tool window to import the changes. 




The procedure above shows the manual way so that you know what happens behind the scenes and where you set up the testing framework. However, if you just start writing tests, IntelliJ IDEA [will automatically detect if the dependency is missing and prompt you to add it](testing.html#add-testing-libraries).

### Write application code

Let's add some code that we'll be testing.

  1. In the Project tool window `Alt+1`, right-click the src/main/java folder and select New | Java Class. Name the class `Calculator.java`.

  2. Paste the following code in the file: 

import java.util.stream.DoubleStream; public class Calculator { static double add(double... operands) { return DoubleStream.of(operands) .sum(); } static double multiply(double... operands) { return DoubleStream.of(operands) .reduce(1, (a, b) -> a * b); } } 




### Create a project

  1. In the main menu, go to File | New | Project.

  2. In the New Project wizard, select Java from the list on the left.

  3. Specify the name for the project, for example, `junit-tutorial`, and select IntelliJ as a build tool.

  4. From the JDK list, select the [JDK](sdk.html#jdk) that you want to use in your project.

If the JDK is installed on your computer, but not defined in the IDE, select Add JDK and specify the path to the JDK home directory.

If you don't have the necessary JDK on your computer, select Download JDK.

  5. Click Create.




### Add dependencies

For our project to use JUnit features, we need to add JUnit as a dependency.

  1. In the main menu, go to File | Project Structure (`Ctrl+Alt+Shift+S`).

  2. Under Project Settings, select Libraries and click ![the New Project Library button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) | From Maven.

  3. In the dialog that opens, specify the necessary library artifact, for example: `org.junit.jupiter:junit-jupiter:5.9.1`.

  4. Apply the changes and close the dialog. 

![Manually adding a testing library to a project](https://resources.jetbrains.com/help/img/idea/2025.3/add-testlib-manually.png)



The procedure above shows the manual way so that you know what happens behind the scenes and where you set up the testing framework. However, if you just start writing tests, IntelliJ IDEA [will automatically detect if the dependency is missing and prompt you to add it](testing.html#add-testing-libraries).

### Create a folder for tests

  1. In the Project tool window `Alt+1`, right-click the top-level folder and select New | Directory.

  2. Name the new directory test.

  3. Right-click the new test directory and select Mark Directory As | Test Sources Root.

The test directory changes the color in the Project tool window to green ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.nodes.testRoot.svg).




By creating a dedicated test folder, you separate test code from production code. This helps the IDE recognize tests, apply the right settings, and organize them consistently. It also ensures that tests are compiled and run correctly without interfering with your main source files.

Learn more from [Test Sources Root](testing.html#add-test-root).

### Write application code

Let's add some code that we'll be testing.

  1. In the Project tool window `Alt+1`, right-click the src folder and select New | Java Class. Name the class `Calculator.java`.

  2. Paste the following code in the file: 

import java.util.stream.DoubleStream; public class Calculator { static double add(double... operands) { return DoubleStream.of(operands) .sum(); } static double multiply(double... operands) { return DoubleStream.of(operands) .reduce(1, (a, b) -> a * b); } } 




### Create tests

Now let's create a test. A test is a piece of code whose function is to check if another piece of code is operating correctly. To do the check, it calls the tested method and compares the result with the predefined expected result. An expected result can be, for example, a specific return value or an exception.

  1. Place the caret at the `Calculator` class declaration and press `Alt+Enter`. Alternatively, right-click it and select Show Context Actions. From the menu, select Create test.

![The code of the class that we are going to test](https://resources.jetbrains.com/help/img/idea/2025.3/junit-tutorial-create-test-1.png)
  2. Select the two class methods that we are going to test.

![The Create Test dialog](https://resources.jetbrains.com/help/img/idea/2025.3/junit-tutorial-create-test-2.png)
  3. The editor takes you to the newly created test class. Modify the `add()` test as follows:

@Test @DisplayName("Add two numbers") void add() { assertEquals(4, Calculator.add(2, 2)); } 

This simple test will check if our method correctly adds 2 and 2. The `@DisplayName` annotation specifies a more convenient and informative name for the test.

  4. Now what if you want to add multiple assertions in a single test and execute all of them regardless of whether some of them fail? Let's do it for the `multiply()` method:

@Test @DisplayName("Multiply two numbers") void multiply() { assertAll(() -> assertEquals(4, Calculator.multiply(2, 2)), () -> assertEquals(-4, Calculator.multiply(2, -2)), () -> assertEquals(4, Calculator.multiply(-2, -2)), () -> assertEquals(0, Calculator.multiply(1, 0))); } 

The `assertAll()` method takes a series of assertions in form of lambda expressions and ensures all of them are checked. This is more convenient than having multiple single assertions because you will always see a granular result rather than the result of the entire test.




To navigate between the test and the code being tested, use the `Ctrl+Shift+T` shortcut.

### Run tests and view their results

After we have set up the code for the testing, we can run the tests and find out if the tested methods are working correctly.

  * To run an individual test, click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.run.run.svg) in the gutter and select Run.

![The popup that appears after clicking on the Run icon in the gutter](https://resources.jetbrains.com/help/img/idea/2025.3/junit_tutorial_run_1.png)
  * To run all tests in a test class, click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.actions.runAll.svg) against the test class declaration and select Run.




You can view test results in the Run tool window.

![The results of the tests shown in the Run tool window](https://resources.jetbrains.com/help/img/idea/2025.3/junit-tutorial-results.png)

30 September 2025

[Testing frameworks](testing-frameworks.html)[Run/Debug configuration: JUnit](run-debug-configuration-junit.html)
