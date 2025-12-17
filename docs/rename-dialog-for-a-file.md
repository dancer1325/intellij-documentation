[//]: # (Source: https://www.jetbrains.com/help/idea/rename-dialog-for-a-file.html)
[//]: # (Downloaded: 2025-12-17 19:57:22)

# Rename dialog for a file

Use this dialog to [rename](rename-refactorings.html) a file.

In addition to renaming the file itself, IntelliJ IDEA can also search for usages of its name. If found, the changes that you make to the file name can also be applied to these usages.

The usages are grouped into categories that correspond to options you can enable or disable.

You can set up a scope for usages of a class where the renaming method is located. For example, it might be helpful if you want to rename some popular method such as `getSomething`. Instead of searching through the whole project and deciding what to rename or what to leave unchanged along the way, you can limit your search to just one file, or just open files, or the recently changed files, and so on.

Item| Description  
---|---  
Rename <file> and its usages to| Specify a new name for the file.  
Search for references| If this option is enabled, IntelliJ IDEA will search for occurrences of the file in references within source code files.In some languages, string literals are treated as references, while in others they are not.  
Search in comments and strings| If this option is enabled, IntelliJ IDEA will look for occurrences of the file in comments and string literals in your source code files.  
Search in loaded sources| If this option is enabled, IntelliJ IDEA will look for occurrences of the file in downloaded object sources.  
Preview pane | The statement to be run to rename the table or column. If necessary, you can edit the statement right in this pane.  
Refactor| Executes the statement and applies the changes immediately.  
Preview| Previews the changes before they are applied.  
Search for text occurrences| If this option is enabled, IntelliJ IDEA will search for occurrences of the file in non-source files, such as text, properties, HTML, or documentation files.  
Rename variables| If this option is on, IntelliJ IDEA will look for occurrences of the file name in the names of variables. Note that only the variables that have the type of the file you are renaming will be taken into account.To illustrate, let's assume that you are renaming the class `MyClass` and there are the variables `MyClass myclass`, `MyClass myclass20`, `MyClass m` and `YourClass myclass25`. In such a case, IntelliJ IDEA will suggest to rename the first and the second of the variables but won't suggest to rename the third and the fourth.  
Rename inheritors| If this option is on, IntelliJ IDEA will look for occurrences of the file name in the names of its inheritors:

  * If you are renaming a class, IntelliJ IDEA will search the hierarchies of the classes that extend this class.
  * If you are renaming an interface, IntelliJ IDEA will search the hierarchies of the interfaces that extend this interface and the hierarchies of the classes that implement this interface.

  
Rename tests| If this option is on, IntelliJ IDEA will look for occurrences of the class name in the names of the test classes.  
Rename bound forms| This option is available if the class you are renaming has an associated GUI form.Select this checkbox to rename the associated form.  
Scope| Use this option to set the scope for the Rename refactoring. For example, limit it to recently changed files, open files, or a custom scope that can be shared or local.  
  
04 November 2024

[Rename dialog for a field](rename-dialog-for-a-field.html)[Rename dialog for a method](rename-dialog-for-a-method.html)
