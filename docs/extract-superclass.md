[//]: # (Source: https://www.jetbrains.com/help/idea/extract-superclass.html)
[//]: # (Downloaded: 2025-12-17 19:26:35)

# Extract superclass

The Extract Superclass refactoring lets you create a superclass for an existing class. You can also rename the original class, so that it becomes an implementation for the newly created superclass. In this case, IntelliJ IDEA changes all original class usages to use a superclass where possible. 

The members of the original class can be moved to the superclass. For a method, you can transfer only the method declaration but not the implementation, declaring the method as abstract in the superclass. As a result, you will have a superclass and the original class inheriting from the superclass.

  1. Open the class in the editor and from the main menu select Refactor | Extract | Superclass.

  2. In the dialog that opens, specify a name for your class, location and class members that you want to include to form your superclass. Select the Make abstract checkbox to leave the method implementation within the current class, and declare it abstract in the extracted superclass. Click Refactor.




24 July 2025

[Extract method](extract-method.html)[Extract parameter](extract-parameter.html)
