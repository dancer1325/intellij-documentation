[//]: # (Source: https://www.jetbrains.com/help/idea/tdd-with-kotlin.html)
[//]: # (Downloaded: 2025-12-17 20:04:01)

## Write the test body

### Create your first test

Given that we’re writing our tests first without necessarily having the code we’re testing available to us yet, we’ll create our first test via the project panel.

  1. Right-click the test root folder ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.nodes.testRoot.svg) and select New | Kotlin Class/File.

In the popup that opens, name the new package and test class: `com.example.demo.CalculatorTest`.

![Test class created](https://resources.jetbrains.com/help/img/idea/2025.3/ij_tdd_create_test_kotlin.png)
  2. Place the caret inside the curly braces in the class, press `Alt+Insert`.

  3. Select Test Function from the menu to create a test function from the default template. Select JUnit 5 as the test framework.

Name the function `testMultiplyBy2`, press `Enter`, and the caret will end up in the function body.

![Creating your first test](https://resources.jetbrains.com/help/img/idea/2025.3/generate-method-kotlin.png)

You can alter the [default test function template](using-file-and-code-templates.html) \- for example, if you wish to change the start of the function name from `test` to `should`.




### Write the test body

It may seem counter-intuitive to write test code for classes and functions that don’t exist, but IntelliJ IDEA makes this straightforward while keeping the compiler happy. IntelliJ IDEA can create classes and functions for you if they don’t already exist.

Write your tests describing what you want to achieve, pressing `Alt+Enter` on any classes that do not exist and selecting Create class. This will give you a minimum implementation that keeps the compiler happy.

  1. Type `val calculator = Calculator()`, press `Alt+Enter`, and select Create class 'Calculator'. 

![Creating a new class](https://resources.jetbrains.com/help/img/idea/2025.3/create-new-class-kotlin.png)
  2. From the Choose class container, select Extract to separate file. In the dialog that opens, select the com.example.demo package in `main` that we have [created earlier](#create-package).

  3. Continue writing the test body, including names of functions that you need that do not exist.

Type `val result = calculator.parse("2 * 2")` and press `Alt+Enter`. Select Create member function to have IntelliJ IDEA create a bare skeleton function.

![Creating a function](https://resources.jetbrains.com/help/img/idea/2025.3/create-function-via-intention.png)
  4. Implement the tested function so that it returns the required type and compiles without issues. The correctness of the result is not important now.

![Implementing the function in the tested class](https://resources.jetbrains.com/help/img/idea/2025.3/implement_function.png)
  5. Add an assertion to the test function. This statement will compare the actual return of the function with the expected one and thus determine the outcome of the test. Type `assertEquals(4, result)`

If the function has not been imported automatically, place the caret at `assertEquals`, press `Alt+Enter`, select Import function, and then select `org.jetbrains.kotlin:kotlin-test`.

![assertEquals\(\) checks if the parameters are equal and fails the test if they are not](https://resources.jetbrains.com/help/img/idea/2025.3/add-assertion.png)


