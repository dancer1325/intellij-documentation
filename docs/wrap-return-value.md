[//]: # (Source: https://www.jetbrains.com/help/idea/wrap-return-value.html)
[//]: # (Downloaded: 2025-12-17 20:07:39)

## Example

Before| After  
---|---  
class Order { String customer; String getCustomer() { return customer; } } |  class Order { String customer; Wrapper getCustomer() { return new Wrapper(customer); } } public class Wrapper { private final String value; public Wrapper(String value) { this.value = value; } public String getValue() { return value; } } 
