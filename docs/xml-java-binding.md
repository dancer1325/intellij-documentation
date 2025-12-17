[//]: # (Source: https://www.jetbrains.com/help/idea/xml-java-binding.html)
[//]: # (Downloaded: 2025-12-17 20:07:41)

# XML-Java Binding

With IntelliJ IDEA, you can get a Java representation of an [XML Schema](https://www.w3schools.com/xml/schema_intro.asp), generate an XML Schema from a Java class, and [unmarshal](http://en.wikipedia.org/wiki/Serialization) XML instance documents into Java content trees and vice versa.

IntelliJ IDEA can use one of the following data binders:

  * [Java Architecture for XML Binding (JAXB)](https://javaee.github.io/jaxb-v2/)

  * [XMLBeans](http://xmlbeans.apache.org/)




### Configure IntelliJ IDEA to use JAXB and XMLBeans

  1. Download and install the XMLBeans tool.

  2. In the Settings dialog (`Ctrl+Alt+S`) , open the Plugins page and install the [Jakarta EE: Web Services (JAX-WS)](https://plugins.jetbrains.com/plugin/18584-jakarta-ee-web-services-jax-ws) plugin.

  3. In the Settings dialog, open the Tools | Web Services page, specify the installation directory of XMLBeans and one of the web services engines.




17 June 2024

[Referencing XML schemas and DTDs](referencing-xml-schemas-and-dtds.html)[Generate Java Code from XML Schema](generating-java-code-from-xml-schema.html)
