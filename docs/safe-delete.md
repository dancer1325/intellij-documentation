[//]: # (Source: https://www.jetbrains.com/help/idea/safe-delete.html)
[//]: # (Downloaded: 2025-12-17 19:59:37)

## Examples

### Safe delete a parameter

Safe delete a parameter for a call hierarchy (here performed on the parameter `i` within `baz(int i)`).

If a parameter is passed only through a call hierarchy, the Safe Delete action will delete the parameter through the whole hierarchy. IntelliJ IDEA displays the appropriate dialog where you can select the caller methods in which the parameter should be deleted.

class CallHierarchySample { private void foo(int i) { bar(i);} private void bar(int i) { baz(i);} private void baz(int i) { } } 

class CallHierarchySample { private void foo() { bar();} private void bar() { baz();} private void baz() { } } 

### Safe delete a method

Safe delete a method in a call hierarchy (here performed on the `foo(int i)` method).

IntelliJ IDEA analyzes the corresponding call hierarchy and displays the appropriate dialog, suggesting you delete all unused methods in that call hierarchy.

class CallHierarchySample { private void foo(int i) { bar(i);} private void bar(int i) { baz(i);} private void baz(int i) { } } 

class CallHierarchySample { } 

### Safe delete the unused class field

Safe delete the unused class field (here performed on `myProperty`).

When you remove an unused class field that is injected via constructor, IntelliJ IDEA removes the associated constructor parameter as well. IntelliJ IDEA opens the appropriate dialog where you can check and confirm your code deletion.

public class MyClass{ private final MyProperty myProperty; public MyClass(MyProperty myProperty){ this.myProperty = myProperty; } } 

public class MyClass { public MyClass(){ } } 
