[//]: # (Source: https://www.jetbrains.com/help/idea/jpa-buddy-database-connections.html)
[//]: # (Downloaded: 2025-12-17 19:30:29)

## Automatic Detection of Data Source Configurations

JPA Buddy offers a convenient way to automatically detect data source configurations from the *.properties file and fills in the required connection settings for you.

![jpa-structure-db-connection](https://resources.jetbrains.com/help/img/idea/2025.3/jpa-structure-db-connection.png)

To use this feature, click on the Detect Connections button in the JPA Structure tab, and JPA Buddy will automatically populate the corresponding fields.

![ij-ultimate-data-sources](https://resources.jetbrains.com/help/img/idea/2025.3/ij-ultimate-data-sources.jpeg)

Starting from version 2023.2, JPA Buddy seamlessly integrates with IntelliJ IDEA Ultimate's robust options for data source configurations. For more information, refer to the relevant [JetBrains documentation page](https://www.jetbrains.com/help/idea/data-sources-and-drivers-dialog.html).

JPA Buddy provides a similar mechanism for the IntelliJ IDEA Community edition.

![ij-community-db-connection](https://resources.jetbrains.com/help/img/idea/2025.3/ij-community-db-connection.jpeg)

It’s worth noting that JPA Buddy is compatible with any property file that adheres to the standard naming convention for property files. This includes YAML files, environment-specific properties files, test-specific properties files, and more. For example, `application.properties`, `application-test.properties`, `application.yaml`, `application-prod.yaml`.
