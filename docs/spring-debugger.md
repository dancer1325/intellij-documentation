[//]: # (Source: https://www.jetbrains.com/help/idea/spring-debugger.html)
[//]: # (Downloaded: 2025-12-17 20:03:01)

## Review the current configuration

Properties defined in a `.properties` are often overridden at runtime, either by another `.properties` file or a bean. If the actual value at runtime is different from the one specified in a `.properties` file, the corresponding line gets an [inlay hint](inlay-hints.html) revealing the actual configuration value.

![The overridden property values are displayed in the application.properties file](https://resources.jetbrains.com/help/img/idea/2025.3/spring-debugger-properties.png)

If a property is defined in multiple contexts, the inlay hint will show multiple definitions

### Navigate to the property redefinition

  * To see which piece of code overrides the property value, click the inlay hint that shows the actual value. The overriding code opens in the editor.

![The inlay hint shows the actual value of a property](https://resources.jetbrains.com/help/img/idea/2025.3/spring-debugger-property-inlay.png)


