[//]: # (Source: https://www.jetbrains.com/help/idea/create-tests.html)
[//]: # (Downloaded: 2025-12-17 19:23:10)

## Create Test dialog controls

Item| Description  
---|---  
Testing library| Select the testing framework that you are going to use.  
Fix| This button is available when a library for the selected testing framework is missing. Click it to download and install the necessary library.If you are using Maven, the IDE will add the missing dependencies to your pom.xml. For Gradle projects, [add the necessary dependencies](testing.html#add-testing-libraries) manually.  
Class name| Enter the name for the test class or accept the default name. You can [change](#naming-pattern-for-tests) the way test classes are named in the settings.  
Superclass| For JUnit3, the superclass `junit.framework.TestCase` is suggested automatically. For the other supported frameworks, this field is blank.  
Destination package| Specify the name of the package where the generated test class will be stored.  
Generate`setUp()/@Before``tearDown()/@After`| Include stub methods for test fixtures and annotations in the generated test class.  
Show inherited methods| Select this option to show all methods, including the inherited ones.  
Generate test methods for| Select the methods for which you want to generate test methods.
