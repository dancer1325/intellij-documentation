[//]: # (Source: https://www.jetbrains.com/help/idea/jpa-buddy-dto-generator.html)
[//]: # (Downloaded: 2025-12-17 19:30:32)

## DTO generation options

When creating DTOs, JPA Buddy provides the flexibility to choose from the following options:

  * Java record – Generates a DTO as a Java record, providing a concise and immutable representation of the DTO with automatic implementations of `equals()`, `hashCode()`, and `toString()`.

  * All args constructor – Generates a constructor that accepts arguments for all fields of the DTO.

  * equals() and hashCode() – Generates the `equals()` and `hashCode()` methods for the DTO based on its fields.

  * toString() – Generates the `toString()` method for the DTO, providing a string representation of its fields.

  * Mutable – By default, the generated DTOs are immutable with final fields and no setters. If you need mutable DTOs with private fields and setters, you can check this option.

  * Fluent setters – This option is available when selecting the Mutable option. It allows the generated setters to return `this` instead of `void`, enabling method chaining for multiple setter calls.

  * Ignore unknown properties for json – Applies the `@JsonIgnoreProperties(ignoreUnknown = true)` annotation to the DTO, allowing it to ignore any unknown properties during JSON deserialization. Only available when the [Jackson Annotations](https://mvnrepository.com/artifact/com.fasterxml.jackson.core/jackson-annotations/2.15.1) dependency is included in the project.


![new-dto-options.png](https://resources.jetbrains.com/help/img/idea/2025.3/new-dto-options.png)
