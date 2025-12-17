[//]: # (Source: https://www.jetbrains.com/help/idea/run-debug-configuration-dartunit.html)
[//]: # (Downloaded: 2025-12-17 19:58:04)

## Dart Test-specific configuration settings

If All in Folder is chosen, the test runner looks for tests only in the files with the names in the format `*_test.dart`.

Item| Description  
---|---  
Test Mode| From this list, choose the scope of tests to run. The available options are:

  * All in File: choose this option to have IntelliJ IDEA run all the tests in a file.
  * All in Folder: choose this option to have IntelliJ IDEA run all the tests from the files in a folder.
  * Group or test by name: choose this option to have IntelliJ IDEA run a specific [test](https://www.dartdocs.org/documentation/test/latest/test/test.html) or a [group](https://www.dartdocs.org/documentation/test/latest/test/group.html) of tests.

Depending on the chosen test scope, specify the path to the test file, test folder, or the name of the test or test group.   
Test runner options| In this area, specify additional [test runner command-line options](https://pub.dev/packages/test#running-tests). For example, to run tests in Chrome, type `-p Chrome`. For more information, refer to [Restricting Tests to Certain Platforms](https://pub.dev/packages/test#restricting-tests-to-certain-platforms).  
VM options| In this field, specify the [options to launch the Dart Virtual Machine with](https://dart.dev/tools/dart-vm#options).  
Environment Variables|  In this field, optionally specify the environment variables for your Dart application. Click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) to open the Environment Variables dialog, where you can create variables and specify their values. You can also copy and paste the contents of the field without opening the Environment Variables dialog. 
