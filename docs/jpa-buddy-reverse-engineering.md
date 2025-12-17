[//]: # (Source: https://www.jetbrains.com/help/idea/jpa-buddy-reverse-engineering.html)
[//]: # (Downloaded: 2025-12-17 19:30:38)

## Entities from DB Wizard

![Entities from DB window](https://resources.jetbrains.com/help/img/idea/2025.3/reverse%20engineering_entities_from_db_window.png)

### Configuration

The menu on the top of the window allows you to configure:

  * [DB connection](jpa-buddy-database-connections.html)

  * Source root and package where the generated entities will be saved

  * Whether indexes and constraints need to be migrated

  * Whether schema name should be specified in the `@Table` annotation




Also, from the Other settings drop-down list, you can move to the [entity declaration](jpa-buddy-entity-designer.html#settings-1) and [reverse engineering](#settings) settings.

### Mapped Relations, Tables and Views

On the left side of the window, you can see:

  * Mapped Relations: tables and views mapped to JPA entities

  * Tables: tables that exist in the DB but are not mapped to entities

  * Views: views that exist in the DB but are not mapped to entities




After selecting any element from the tree, a panel for migrating attributes from columns will appear. Also, you will be able to define a class name in the corresponding field.

### Migrating Attributes

The main part of the window allows you to configure everything related to attributes. You can choose which attributes you want to add and change all their params, except Column Name. Mapping type and attribute/converter/hibernate types are represented as drop-down lists.

All attributes are divided into 3 categories:

  * Migrated Columns - columns that are already present in the entity (available only for mapped relations)

  * Columns - new columns that are not yet mapped in the entity or parent @MappedSuperclass

  * References - optional associations that are not represented as a column in the observed table




#### Parent Entities

IntelliJ IDEA offers the ability to define a parent entity by selecting a class annotated with `@MappedSuperclass` from the Parent drop-down box. This allows the generated entities to extend from the parent class and automatically inherit all attributes that have the same name and type.

In cases where the column name in the `@MappedSuperclass` doesn't match the child entity's table, we can still inherit the attribute using the `@AttributeOverride` annotation. By simply selecting the attribute name and choosing the one to override, IntelliJ IDEA assists in managing the inheritance.

![attribute-override.png](https://resources.jetbrains.com/help/img/idea/2025.3/attribute-override.png)

During entity generation, IntelliJ IDEA alerts us if any inherited attributes from the `@MappedSuperclass` are missing in the database. To align the model with the database, access the Generate DDL by Entities action in the JPA Structure menu and select the Existing DB update option.

#### Creating Enums

For attributes matching the `String` or `Integer` type, you can change the mapping type from Basic to Enum, and IntelliJ IDEA will create the corresponding Enum class in the project. You need to fill the enum with proper values manually.

#### Dealing With Unknown Types

For some SQL types, there is no exact match to Java classes. In this case, IntelliJ IDEA does not set the type to prevent generating non-working code. You will need to choose the attribute type yourself. You can also configure default type mappings for each DBMS in the [settings](#type-mappings).

If you have the [HibernateTypes](https://github.com/vladmihalcea/hibernate-types) library in your project dependencies list, IntelliJ IDEA can automatically suggest suitable types from the library for the unsupported SQL types during reverse engineering:

#### // TODO Comments

If you want to postpone an attribute creation for specific columns, you can choose `//todo` comment as the mapping type. IntelliJ IDEA will generate the `//todo` comment with the corresponding quick-fix actions depending on the column type. You can call these actions by pressing `Ctrl+B`:

  * For known basic and association types you can:

    * Uncomment as is

    * Remove column mapping

  * For unknown column type you can:

    * Define target Java type

    * Uncomment as is

    * Remove column mapping




Here is an example of generated `//todo` comment for the attribute with an unknown column type:

/* TODO [Reverse Engineering] create field to map the 'description' column Available actions: Define target Java type | Uncomment as is | Remove column mapping @Column(name = "description", columnDefinition = "jsonb") private java.lang.Object description; */ 

After calling the Define target Java type action, the following window will appear:

![mapping-java-type](https://resources.jetbrains.com/help/img/idea/2025.3/mapping-java-type.png)

IntelliJ IDEA will remember data mappings for the subsequent reverse engineering actions. You can always change them in the [settings](#type-mappings).

### Map DB Views to JPA Entities

IntelliJ IDEA follows all best practices providing the most efficient mapping for DB views while reverse engineering:

  1. As DB views do not have a primary key, IntelliJ IDEA allows you to select a field or a set of fields to use as the identifier for the target entity.

  2. Most DB views are immutable. So, IntelliJ IDEA adds `@Immutable` annotation to the entity and generates getters only. This helps to improve application performance.

  3. IntelliJ IDEA generates only a no-arg protected constructor for entities that are mapped to a DB view, as per JPA specifications, which prevents developers from creating a new instance of such entities in the business logic code



