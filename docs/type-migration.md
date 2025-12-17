[//]: # (Source: https://www.jetbrains.com/help/idea/type-migration.html)
[//]: # (Downloaded: 2025-12-17 20:04:52)

## Examples

`f: int -> String`

Before| After  
---|---  
int f; void bar(int i) {} void foo() { bar(f); } |  String f; void bar(String i) {} void foo() { bar(f); }   
  
`I<String> -> I<Integer>`

Before| After  
---|---  
interface I<T> { T foo(T t); } class A implements I<String> { String myString; public String foo(final String s) { if (s == null) { return myString; } return s; } } |  interface I<T> { T foo(T t); } class A implements I<Integer> { Integer myString; public Integer foo(final Integer s) { if (s == null) { return myString; } return s; } }   
  
`myResult: ArrayList<String> -> String[]`

Before| After  
---|---  
public class ResultContainer { private ArrayList<String> myResult; public String[] getResult() { return myResult.toArray(new String[myResult.size()]); } } |  public class ResultContainer { private String[] myResult; public String[] getResult() { return myResult; } } 
