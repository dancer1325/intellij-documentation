[//]: # (Source: https://www.jetbrains.com/help/idea/remove-middleman.html)
[//]: # (Downloaded: 2025-12-17 19:57:17)

## Example

Before| After  
---|---  
// File Foo.java public class Foo { Bar bar; public Foo getImpValue() { return bar.getImpValue(); } } // File Bar.java public class Bar { private Foo impValue1; public Bar(Foo impValue) { impValue1 = impValue; } public Foo getImpValue() { return impValue1; } } // File Client.java public class Client { Foo a; Foo impValue = a.getImpValue(); } |  // File Foo.java public class Foo { Bar bar; public Bar getbar() { return bar; } } // File Bar.java public class Bar { private Foo impValue1; public Bar(Foo impValue) { impValue1 = impValue; } public Foo getImpValue(){ return impValue1; } } // File Client.java public class Client { Foo a; Foo impValue = a.getbar().getImpValue(); } 
