[//]: # (Source: https://www.jetbrains.com/help/idea/make-method-static.html)
[//]: # (Downloaded: 2025-12-17 19:31:43)

## Make method static examples

Before| After  
---|---  
class ConnectionPool { public int i; public int j; public void getConnection() { ... } } |  class ConnectionPool { public int i; public int j; public static void getConnection(ConnectionPool connectionPool) { ... } }   
class ConnectionPool { public int i; public int j; public void getConnection() { ... } } |  class ConnectionPool { public int i; public int j; public static void getConnection(int i, int j) { ... } }   
  
In call hierarchies, if the method callers don't contain any other references to instance members, IntelliJ IDEA suggests that you make those callers static too. In this example, the refactoring is performed on `baz(int i)`. All the caller methods are selected for making static too. The appropriate dialog lets you select the caller methods to be made static.

Before| After  
---|---  
class CallHierarchySample { private void foo(int i) { bar(i);} private void bar(int i) { baz(i);} private void baz(int i) { } } |  class CallHierarchySample { private static void foo(int i) { bar(i);} private static void bar(int i) { baz(i);} private static void baz(int i) { } } 
