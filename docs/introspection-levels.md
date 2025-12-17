[//]: # (Source: https://www.jetbrains.com/help/idea/introspection-levels.html)
[//]: # (Downloaded: 2025-12-17 19:30:01)

## Introspection level defaults

By default, IntelliJ IDEA automatically sets the default introspection level for each schema based on the schema type and number of objects. For each schema the introspector counts objects and selects the introspection level using the following thresholds, where N is the number of objects:

Schema| Level 3| Level 2| Level 1  
---|---|---|---  
Current| N <= 1000| N <= 3000| Otherwise  
Non-current| Never| N <= 3000| Otherwise  
System| Never| N <= 100| Otherwise  
  
The [current schema](schemas.html#set_default_schema_query_console) is the one the [session](managing-connection-sessions.html) is connected to.

To change the defaults, open the Data Sources and Drivers dialog ( `Shift+Enter`) , navigate to Options | Introspection | Default level, and select the default introspection level for your data source.

![Change the introspection level defaults](https://resources.jetbrains.com/help/img/idea/2025.3/db_oracle_introspection_level_defaults.png)
