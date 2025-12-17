[//]: # (Source: https://www.jetbrains.com/help/idea/spring-projects.html)
[//]: # (Downloaded: 2025-12-17 20:03:07)

## Configure a parent context

IntelliJ IDEA allows you to configure a parent-child relationship between contexts. Beans from a parent context are visible to beans in child contexts, but not vice versa. Therefore, beans from child contexts can use configuration from the parent context.

For example, Spring MVC applications usually have two contexts: one for the web layer beans and the other for services and repositories. The web layer context will be a child context in this case, as you need to inject services into controllers, not the other way around.

To configure a parent context, use the New Application Context dialog, as described in [Create application contexts](#create-application-context).

The Multiple Contexts panel shows up on top of the editor for files included in two or more application contexts. You can use this panel to select the active context, for example, if you want to run your application with a specific configuration, and change highlighting. To disable the panel, click ![The Settings button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.settings.svg) and clear the Show Multiple Contexts panel checkbox.

IntelliJ IDEA can configure the parent context automatically. For example, if the IDE detects the Spring Cloud context, it will make it a parent application context for Spring Boot.
