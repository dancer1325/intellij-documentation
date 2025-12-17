[//]: # (Source: https://www.jetbrains.com/help/idea/persistence-tool-window.html)
[//]: # (Downloaded: 2025-12-17 19:33:53)

## Generate entities from database

With IntelliJ IDEA, you can create JPA entity classes and attributes based on an existing database schema. This functionality relies on the [Reverse Engineering](jpa-buddy-reverse-engineering.html) plugin, which is bundled in IntelliJ IDEA Ultimate.

### Generate JPA entities from database

  1. If a database connection is not established, [create one](connecting-to-a-database.html).

In Spring, Micronaut, and Quarkus projects, you can quickly create a database connection right from your application.properties or application.yml file by clicking ![Datasource icon](https://resources.jetbrains.com/help/img/idea/2025.3/javaee-persistence-impl.icons.expui.add-db-from-config.svg) in the gutter.

  2. In the Persistence tool window, expand the JPA node, right-click an element, and select New | JPA Entities from DB.

Alternatively, right-click a database connection in the Database tool window, and select Create JPA Entities from DB.

  3. Select a database connection, tables, and attributes to be mapped. For more information, refer to [Entities from DB Wizard](jpa-buddy-reverse-engineering.html#entities-from-db-wizard).




While your IDE is open, the database can be modified by other clients. To get the latest data from the database, you can click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.refresh.svg) in either the Entities from DB window or in the Database tool window.

### Generate attributes from database

You can also generate attributes for an existing class based on a database table.

  1. If a database connection is not established, [create one](connecting-to-a-database.html).

  2. In the Persistence tool window, expand the JPA node, right-click an entity and select New | JPA Entities from DB.

Alternatively, right-click a database connection in the Database tool window, and select Create JPA Attributes from DB.

  3. Select a database connection, a table or a view, and columns to be mapped. The attributes migration flow is identical to what is described in the [Entities from DB wizard](jpa-buddy-reverse-engineering.html#migrating-attributes) section.

![Entity attributes from DB dialog](https://resources.jetbrains.com/help/img/idea/2025.3/jpa_attributes_from_db.png)


