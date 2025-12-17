[//]: # (Source: https://www.jetbrains.com/help/idea/encapsulate-fields.html)
[//]: # (Downloaded: 2025-12-17 19:25:49)

## Examples

Before| After  
---|---  
//File Class.java public class Class { public String aString; } |  //File Class.java public class Class { private String aString; public void setaString(String aString) { this.aString = aString; } public String getaString() { return aString; } }   
//File AnotherClass.java public class AnotherClass { public Class aClass; public void method() { aClass.aString="string"; } } |  //File AnotherClass.java public class AnotherClass { public Class aClass; public void method() { aClass.setaString("string"); } } 
