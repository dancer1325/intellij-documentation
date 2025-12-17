[//]: # (Source: https://www.jetbrains.com/help/idea/jpa-buddy.html)
[//]: # (Downloaded: 2025-12-17 19:30:40)

## Dependencies

JPA Buddy scans the project dependencies and enables the corresponding features. In a multi-module project, features are enabled based on the presence of the dependency within the module, not the entire project.

Every time you add dependencies in the Maven or Gradle build script, click ![Load the changes](https://resources.jetbrains.com/help/img/idea/2025.3/maven.images.expui.build.mavenLoadChanges.svg) Load Maven Changes or ![Load the changes](https://resources.jetbrains.com/help/img/idea/2025.3/gradle.icons.expui.gradleLoadChanges.svg) Sync Gradle Changes in the top-right part of the editor or press `Ctrl+Shift+O`.

Dependency| Features  
---|---  
[Hibernate](https://mvnrepository.com/artifact/org.hibernate/hibernate-core)| 

  * Create and edit entities, entity attributes, lifecycle callbacks, indexes, and constraints in both Java and Kotlin.
  * Assign JPA converters and Hibernate custom types.
  * Apply Lombok annotations to entities.
  * Generate proper equals, hashCode, and toString.

  
[EclipseLink](https://mvnrepository.com/artifact/org.eclipse.persistence/eclipselink)  
[Spring Data JPA](https://mvnrepository.com/artifact/org.springframework.data/spring-data-jpa)| 

  * Create repositories for entities.
  * Generate queries using visual constructors.
  * Extract JPQL from derived method queries.
  * Pick which fields to return from queries and generate projections.

  
[Hibernate Validator](https://mvnrepository.com/artifact/org.hibernate.validator/hibernate-validator)| Add Hibernate Validator annotations to Entity and DTO attributes via JPA Designer and DTO generator wizard respectively.  
[Spring Boot Starter Validation](https://mvnrepository.com/artifact/org.springframework.boot/spring-boot-starter-validation)  
[Hibernate Types](https://mvnrepository.com/artifact/com.vladmihalcea/hibernate-types-52)| Assign Hibernate Custom Types to attributes via a code inspection with a quick fix (`Alt+Enter`).  
[Liquibase](https://mvnrepository.com/artifact/org.liquibase/liquibase-core)| 

  * Automatically generate Liquibase changelogs by comparing JPA model to a target database, model to snapshot, or DB to DB.
  * Use visual designers for Liquibase changelogs
  * Use coding assistance and autocomplete in Liquibase changelogs for table and column names. JPA Buddy takes these values directly from your data model.

  
[Flyway](https://mvnrepository.com/artifact/org.flywaydb/flyway-core)| 

  * Generate Flyway migrations by comparing JPA model to a target database, model to snapshot, or DB to DB.
  * Scaffold INSERT, UPDATE, and DELETE statements for your entities in SQL files.

  
[MapStruct](https://mvnrepository.com/artifact/org.mapstruct/mapstruct)| Create MapStruct mappers to convert entities to DTOs and back.  
[Blazebit Persistence Entity View API](https://mvnrepository.com/artifact/com.blazebit/blaze-persistence-entity-view-api)| Create Blaze Persistence Entity View for JPA Entity.  
[Blazebit Persistence Integration Spring Data Base](https://mvnrepository.com/artifact/com.blazebit/blaze-persistence-integration-spring-data-base)| Create Spring Data JPA repository for Blaze Persistence Entity View.  
[Hibernate Envers](https://mvnrepository.com/artifact/org.hibernate/hibernate-envers)| 

  * Generate database migration scripts for audit tables.
  * Create Spring Data JPA revision repositories.
  * Annotate entities and their fields for auditing via JPA Designer.
  * Generate @RevisionEntity via convenient wizard.


