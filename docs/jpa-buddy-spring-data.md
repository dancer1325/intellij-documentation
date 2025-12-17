[//]: # (Source: https://www.jetbrains.com/help/idea/jpa-buddy-spring-data.html)
[//]: # (Downloaded: 2025-12-17 19:30:39)

## Repository Creation

JPA Buddy provides various ways to create repositories to make working with JPA-related objects more convenient for most users. All possible ways to generate repositories in the project are shown in the following video:

You can create a Spring Data JPA repository only for an entity with a field annotated with `@Id`.

In the New JPA Repository window, you can set:

  * The entity for which the repository will be created

  * The name of the repository class

  * The parent class for the repository. It can be:

    * A repository from the [org.springframework.data.repository](https://docs.spring.io/spring-data/jpa/docs/current/reference/html/#jpa.repositories) package

    * Any repository from your project

  * Whether the repository will extend [JpaSpecificationExecutor](https://docs.spring.io/spring-data/jpa/docs/current/reference/html/#specifications) or not

  * The source root

  * The package where the repository will be created


![new-jpa-repository](https://resources.jetbrains.com/help/img/idea/2025.3/new-jpa-repository-single.png)

Creating Spring Data repositories one by one for each entity can become a tedious job. With JPA Buddy, you can speed up this process. To create repositories for multiple JPA entities at once, you need to take three steps. Select the entities in the project tree, invoke the JPA Buddy wizard, then adjust your selection. That's it! Look at how this feature can accelerate the development process:
