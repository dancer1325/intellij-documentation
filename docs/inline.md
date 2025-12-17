[//]: # (Source: https://www.jetbrains.com/help/idea/inline.html)
[//]: # (Downloaded: 2025-12-17 19:29:31)

## Examples

### Inline Variable

Inline Variable refactoring replaces redundant variable usage with its initializer.

The variable must be initialized at declaration. If the initial value is modified somewhere in the code, only the occurrences before modification will be inlined.

Example 1

public void method() { int number = anotherClass.intValue(); int b = a + number; } 

public void method() { int b = a + anotherClass.intValue(); } 

Example 2

public void method() { AnotherClass.InnerClass aClass = anotherClass.innerClass; int a = aClass.i; } 

public void method() { int a = anotherClass.innerClass.i; } 

### Inline Method

Inline Method results in placing the method's body into the body of its caller(s).

Example 1

public void method() { int c=add(a,b); int d=add(a,c); } private int add(int a, int b) { return a+b; } 

public void method() { int c= a + b; int d= a + c; } 

Example 2

public ArrayList method() { String[] strings = {"a","b","c"}; ArrayList list=add(strings); return list; } private ArrayList add(String[] strings) { ArrayList list = new ArrayList(); for (int i=0; i< strings.length; i++) {list.add(strings[i]);} return list; } 

public ArrayList method() { String[] strings = {"a","ab","abc"}; ArrayList list1 = new ArrayList(); for (int i=0; i< strings.length; i++) {list.add(strings[i]);} ArrayList list = list1; return list; } 

### Inline Abstract Method

Inlining an abstract method that has exactly one implementation replaces calls to the method with the concrete implementation's code and removes the need for the method declaration and its call.

public interface AnInterface { int readValue(); } class AClass implements AnInterface { public int readValue() { return 1; } } class UserClass{ void doSmth(){ AnInterface a = new AClass(); int i = a.readValue(); } } 

public interface AnInterface { int readValue(); } class AClass implements AnInterface { public int readValue() { return 1; } } class UserClass{ void doSmth(){ AnInterface a = new AClass(); int i =1; } } 

### Inline Constructor

Inline Constructor allows compressing a chain of constructors if one of them is a special case of another.

public class Class { public int varInt; public Class() { this(0); } public Class(int i) { varInt=i; } public void method() { Class aClass=new Class(); } } 

public class Class { public int varInt; public Class(int i) { varInt=i; } public void method() { Class aClass=new Class(0); } } 

### Inline Superclass

The Inline Superclass refactoring results in pushing superclass' methods into the class where they are used and removing the superclass.

public class Bar { ... int calculations1() { ... } int calculations2() { ... } } class Foo extends Bar { int someMethod() { ... if (something > calculations1()) { ... return calculations2(); } ... } } 

public class Bar { ... int calculations1() { ... } int calculations2() { ... } } class Foo extends Bar { int someMethod() { ... if (something > calculations1()) { ... return calculations2(); } ... } } 

### Inline to Anonymous Class

Inline to Anonymous Class refactoring allows replacing a redundant class with its contents. Starting with Java 8, the inlined anonymous classes can be converted to lambdas automatically.

import java.util.*; public class Main { public class MyComparator implements Comparator<String> { @Override public int compare(String s1, String s2) { return 0; } } void sort(List<String> scores) { scores.sort(new MyComparator()); } } 

import java.util.*; public class Main { void sort(List<String> scores) { scores.sort((s1, s2) -> 0); } } 

### Inline Parameter

The Inline Parameter refactoring allows you to replace usages of the parameter with the value from the arguments of the method call.

public class HelloWorld { public static void main(String[] args) { int score = getScore(5); System.out.println("Score: " + score); } public static int getScore(int base) { return base * 10; } } 

public class HelloWorld { public static void main(String[] args) { int score = getScore(); System.out.println("Score: " + score); } public static int getScore() { return 5 * 10; } } 
