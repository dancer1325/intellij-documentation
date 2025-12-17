[//]: # (Source: https://www.jetbrains.com/help/idea/spring-support-tutorial.html)
[//]: # (Downloaded: 2025-12-17 20:03:09)

## Productivity tips

### Quickly inject beans

IntelliJ IDEA provides a number of ways to quickly inject beans, which saves you from having to manually type annotations and fields or constructors.

  1. Within a Spring component, start typing a bean name.

  2. Use one of the following ways to get the needed bean:

     * Press `Alt+Enter` and select Add dependency with name matching 'bean name'.

     * Start typing a bean name and enter `.autowire` to invoke the [postfix completion template](postfix-code-completion.html). For example, enter `custom.autowire` to find beans that start with `custom`.

  3. If the entered name matches exactly the name of a bean, it will be injected right away. If it matches only a part of the name, you can select the needed bean from the Select Bean window that opens. 

![Bean injection](https://resources.jetbrains.com/help/img/idea/2025.3/spring_select_bean.png)



If a class has fields annotated with `@Autowire`, this will add a new `@Autowire` field. Otherwise, it will add the corresponding parameter to the class constructor.

Alternatively, you can press `Alt+Insert` and select the injection type from the Generate context menu: @Autowired Dependency, Constructor Dependency, or Setter Dependency. Unlike the method described above, this method lets you select a way to inject a bean and does not filter the beans, so you can preview all of them.

### Navigate to secure URL

If you use [Spring Security](https://docs.spring.io/spring-security/reference/index.html), you may have security rules in place, such as allowing access to URLs for authenticated users only or for users with specific roles. IntelliJ IDEA provides navigation from security matchers to Spring controllers and from controllers to security matchers.

  * To navigate to a controller method from a Spring security matcher, click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.inlaySecuredShield.svg) next to the matcher (such as `antMatchers`, `mvcMatchers`, `requestMatchers` in Spring Security before 5.8 or `securityMatcher` in Spring Security 5.8 and higher, or in XML URL patterns).

  * To check the security configuration for a controller (and navigate to this configuration if it's available), click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.inlayGlobe.svg) next to the controller URL and select Show security configurations for URL.


![Spring Security URL mapping](https://resources.jetbrains.com/help/img/idea/2025.3/spring_security_url_mapping.png)

To disable the ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.inlaySecuredShield.svg) inlay hint icons, press `Alt+Enter` next to the icon and select Hide secured URLs inlays. To disable the ![](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.inlayGlobe.svg) inlay hint icons, press `Alt+Enter` next to the icon and select Hide URL path inlays for current language.

To enable them back, open the IDE settings (`Ctrl+Alt+S`), go to Editor | Inlay Hints, and select the needed checkboxes under URL path.

### Quickly create a connection to a database

Using the Database Tools and SQL plugin, IntelliJ IDEA lets you create and manage [connections to databases](connecting-to-a-database.html).

In a Spring Boot project, you can instantly create it from your application properties file.

  1. Open an application.properties or application.yml file. If it contains datasource-related properties (for example, `spring.datasource.url`) , the datasource icon ![Datasource icon](https://resources.jetbrains.com/help/img/idea/2025.3/javaee-persistence-impl.icons.expui.add-db-from-config.svg) will be displayed in the gutter.

  2. Click ![Datasource icon](https://resources.jetbrains.com/help/img/idea/2025.3/javaee-persistence-impl.icons.expui.add-db-from-config.svg). This will open the data source creation form with datasource parameters (such as URL, username, or database name) populated based on data from your configuration file.

If the data source is already configured, the datasource icon ![](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.dbms.svg) is displayed instead. Click it to open the datasource in the Database tool window.

![Create data source window](https://resources.jetbrains.com/help/img/idea/2025.3/spring_create_datasource_from_properties.png)



Below is the list of databases for which this action is available:

  * Amazon Redshift

  * Apache Cassandra

  * Apache Derby

  * Couchbase

  * H2

  * HSQLDB

  * IBM Db2

  * MariaDB

  * Microsoft SQL Server

  * MongoDB

  * MySQL

  * Oracle Database

  * PostgreSQL

  * Redis

  * SQLite

  * Sybase




For more details on data source parameters, refer to [Data sources](managing-data-sources.html).
