[//]: # (Source: https://www.jetbrains.com/help/idea/using-the-testify-toolkit.html)
[//]: # (Downloaded: 2025-12-17 20:05:50)

# Using the Testify toolkit

The `github.com/stretchr/testify` package is a popular Go library used for writing unit tests. It provides a set of tools like assertions, mocks, and suites that make it easier to write tests in Go. With Testify, you can run your suites and methods as regular test functions. For more information about the toolkit, refer to the description of [Testify on GitHub](https://github.com/stretchr/testify).

In this tutorial, we will generate and use tests for the following application in the main.go file:

package math // Add returns the sum of two integers. func Add(a, b int) int { return a + b } 

### Generate a test for package

  1. Open a Go file for which you want to generate a test.

  2. In the main menu, click Code | Generate.

  3. In the Generate pop-up window, select Tests for package.

IntelliJ IDEA creates _test.go file with a table test template.




Modify the generated test so it uses the testify toolkit. Consider the following code snippet for the test.

package math import ( "github.com/stretchr/testify/assert" "testing" ) func TestAdd(t *testing.T) { type args struct { a int b int } tests := []struct { name string args args want int }{ {"add positives", args{1, 2}, 3}, {"add negatives", args{-1, -2}, -3}, {"add positive and negative", args{-1, 1}, 1}, {"add zeros", args{0, 0}, 0}, } for _, tt := range tests { t.Run(tt.name, func(t *testing.T) { result := Add(tt.args.a, tt.args.b) assert.Equal(t, tt.want, result, "they should be equal") }) } } 

IntelliJ IDEA has automatically added the following import declaration: `"github.com/stretchr/testify/assert"`.

### Synchronize missing dependencies

  1. Click the import declaration that is missing.

  2. Press `Alt+Enter` and select Fix missing dependencies.




### Run tests with testify

  * Click the Run test icon ![The Run test icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.execute.svg) and select Run <configuration>.

You can also run individual table tests if desired.

[![Run tests with Testify](https://resources.jetbrains.com/help/img/idea/2025.3/go_run_testify.png)](https://resources.jetbrains.com/help/img/idea/2025.3/go_run_testify.png)



### Compare expected and actual values

You can compare expected and actual values for failed assertion tests.

  * You can compare expected and actual values for failed assertion tests. To see the difference, click the Click to see difference link in the Run pane.

![Compare expected and actual values](https://resources.jetbrains.com/help/img/idea/2025.3/go_compare_expected_actual_results.png)
  * Right-click the failed test and select View Differences. Alternatively, press `Ctrl+D`.

![Compare expected and actual values](https://resources.jetbrains.com/help/img/idea/2025.3/go_compare_expected_actual_results_context_menu.png)



26 May 2024

[Testing](go-plugin-test-configurations.html)[JSON](json.html)
