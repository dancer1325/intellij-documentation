[//]: # (Source: https://www.jetbrains.com/help/idea/rename-dialog-for-a-class-or-an-interface.html)
[//]: # (Downloaded: 2025-12-17 19:57:18)

# Rename dialog for a class or an interface

Use this dialog to [rename](rename-refactorings.html) a class or an interface.

In addition to renaming the class or the interface itself, IntelliJ IDEA can also search for usages of its name. If found, the changes that you make to the class or the interface name can also be applied to these usages.

The usages are grouped into categories that correspond to options you can enable or disable.

You can set up a scope for usages of a class where the renaming method is located. For example, it might be helpful if you want to rename some popular method such as `getSomething`. Instead of searching through the whole project and deciding what to rename or what to leave unchanged along the way, you can limit your search to just one file, or just open files, or the recently changed files, and so on.

Item| Description  
---|---  
Rename <class or interface> and its usages to| Specify a new name for the class or the interface.  
Search for references| If this option is enabled, IntelliJ IDEA will search for occurrences of the class or the interface in references within source code files.In some languages, string literals are treated as references, while in others they are not.  
Search in comments and strings| If this option is enabled, IntelliJ IDEA will look for occurrences of the class or the interface in comments and string literals in your source code files.  
Search in loaded sources| If this option is enabled, IntelliJ IDEA will look for occurrences of the class or the interface in downloaded object sources.  
Preview pane | The statement to be run to rename the table or column. If necessary, you can edit the statement right in this pane.  
Refactor| Executes the statement and applies the changes immediately.  
Preview| Previews the changes before they are applied.  
Search for text occurrences| If this option is enabled, IntelliJ IDEA will search for occurrences of the class or the interface in non-source files, such as text, properties, HTML, or documentation files.  
Rename variables| If this option is on, IntelliJ IDEA will look for occurrences of the class or the interface name in the names of variables. Note that only the variables that have the type of the class or the interface you are renaming will be taken into account.To illustrate, let's assume that you are renaming the class `MyClass` and there are the variables `MyClass myclass`, `MyClass myclass20`, `MyClass m` and `YourClass myclass25`. In such a case, IntelliJ IDEA will suggest to rename the first and the second of the variables but won't suggest to rename the third and the fourth.  
Rename inheritors| If this option is on, IntelliJ IDEA will look for occurrences of the class or the interface name in the names of its inheritors:

  * If you are renaming a class, IntelliJ IDEA will search the hierarchies of the classes that extend this class.
  * If you are renaming an interface, IntelliJ IDEA will search the hierarchies of the interfaces that extend this interface and the hierarchies of the classes that implement this interface.

  
Rename tests| If this option is on, IntelliJ IDEA will look for occurrences of the class name in the names of the test classes.  
Rename bound forms| This option is available if the class you are renaming has an associated GUI form.Select this checkbox to rename the associated form.  
Scope| Use this option to set the scope for the Rename refactoring. For example, limit it to recently changed files, open files, or a custom scope that can be shared or local.  
  
08 October 2024

[Rename dialogs](rename-dialogs.html)[Rename dialog for a directory](rename-dialog-for-a-directory.html)
