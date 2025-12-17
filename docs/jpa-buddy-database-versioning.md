[//]: # (Source: https://www.jetbrains.com/help/idea/jpa-buddy-database-versioning.html)
[//]: # (Downloaded: 2025-12-17 19:30:30)

## Database first

In this approach, the database takes precedence over data model classes (POJOs or JPA entities), which are generated from the database schema through code generation, also known as "Database reverse engineering." It's essential to avoid altering the generated classes since they can be regenerated at any time, and any changes made in the source code will be lost. However, this approach **does not eliminate the need for migration script generation** , as they are necessary for upgrading existing installations to the latest version.
