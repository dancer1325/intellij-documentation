[//]: # (Source: https://www.jetbrains.com/help/idea/jpa-buddy-coding-assistance.html)
[//]: # (Downloaded: 2025-12-17 19:30:28)

## Code Completion

### Generate & Inject Spring Data JPA Repositories

To create a new Spring Data JPA repository just start typing the repository name that begins with the entity name (1). Then, the [repository wizard](jpa-buddy-spring-data.html#repository-creation) will open.

By following the same coding style, you can also inject an existing Spring Data JPA repository (2). Just start typing the existing repository name and JPA Buddy will find it.

![spring-data-jpa-repository-generation-injection](https://resources.jetbrains.com/help/img/idea/2025.3/spring-data-jpa-repository-generation-injection.png)

According to your [injection settings](#settings), JPA Buddy will inject the repository into the current class. The example below shows constructor-based injection:

![spring-data-jpa-repository-generation-injection](https://resources.jetbrains.com/help/img/idea/2025.3/repository-injection-result.png)

#### Generate & Call Methods/Queries

With JPA Buddy, you don't need to switch focus between multiple editors. It allows you to call [query visual designers](jpa-buddy-spring-data.html#example) right from here:

![repository-methods-generation](https://resources.jetbrains.com/help/img/idea/2025.3/repository-methods-generation.png)

Also, you can find/create repository methods via entity class name call:

![entity-class-name-method-call](https://resources.jetbrains.com/help/img/idea/2025.3/entity-class-name-method-call.png)

### Generate & Inject MapStruct Mappers

JPA Buddy is able to generate MapStruct mapper, inject it, and scaffold a proper mapping call. Use "mapTo..." option to [generate a new mapper](jpa-buddy-dto-generator.html#mapstruct-support), or apply methods from existing ones (e.g., mapToPetDto for the example below). This feature works for both: single instances and collections of entities or DTOs.

![map-to-postfix](https://resources.jetbrains.com/help/img/idea/2025.3/map-to-postfix.png)

Here is the code that JPA Buddy will generate after selecting the mapToPetDto option:

![map-to-result](https://resources.jetbrains.com/help/img/idea/2025.3/map-to-result.png)
