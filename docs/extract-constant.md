[//]: # (Source: https://www.jetbrains.com/help/idea/extract-constant.html)
[//]: # (Downloaded: 2025-12-17 19:26:15)

## Example

Let's introduce a constant for the expression `"string"` that occurs twice throughout code.

public class Class { public void method() { ArrayList list = new ArrayList(); list.add("string"); anotherMethod("string"); } private void anotherMethod(String string) { } } 

IntelliJ IDEA extracts the constant and replaces the expression with the constant `STRING`.

public class Class { private static final String STRING = "string"; public void method() { ArrayList list = new ArrayList(); list.add(STRING); anotherMethod(STRING); } private void anotherMethod(String string) { } } 
