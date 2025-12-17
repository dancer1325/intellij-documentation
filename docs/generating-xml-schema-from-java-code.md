[//]: # (Source: https://www.jetbrains.com/help/idea/generating-xml-schema-from-java-code.html)
[//]: # (Downloaded: 2025-12-17 19:27:48)

# Generate an XML Schema from Java Code

This topic describes how to have an [XML Schema](https://www.w3schools.com/xml/schema_intro.asp) generated on the basis of a Java class, which involves mapping the members of the Java class to the elements of the XML Schema. With IntelliJ IDEA, this transformation can be done using the JAXB.

### Install the Jakarta EE: Web Services (JAX-WS) plugin

This functionality relies on the [Jakarta EE: Web Services (JAX-WS)](https://plugins.jetbrains.com/plugin/18584-jakarta-ee-web-services-jax-ws) plugin, which you need to install and enable. 

The Jakarta EE: Web Services (JAX-WS) plugin is not available in IntelliJ IDEA without the Ultimate subscription. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Marketplace tab, find the Jakarta EE: Web Services (JAX-WS) plugin, and click Install (restart the IDE if prompted).




### Generate an XML Schema from a Java class using JAXB

  1. Open the necessary class in the editor.

  2. In the main menu, go to Tools | XML Actions | Generate XML Schema From Java Using JAXB.

  3. In the dialog that opens, specify the method parameter and return types to be reflected in the generated Schema:

     * To have all the class methods involved, clear the Include parameter and return type of the following methods checkbox.

     * To select specific methods to be involved, select the Include parameter and return type of the following methods checkbox, then select the Add to JAXB generation checkbox next to the desired methods.




18 July 2025

[Generate Java Code from XML Schema](generating-java-code-from-xml-schema.html)[XML refactorings](xml-refactorings.html)
