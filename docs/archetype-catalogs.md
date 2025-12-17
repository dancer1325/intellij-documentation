[//]: # (Source: https://www.jetbrains.com/help/idea/archetype-catalogs.html)
[//]: # (Downloaded: 2025-12-17 19:18:29)

# Archetype Catalogs

Use this page to configure or modify Maven [archetype catalogs](maven-support.html#maven_archetype).

Icon| Description  
---|---  
![the Add the Add icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) or `Alt+Insert`| Use this icon or shortcut to define a new catalog. Specify a name and a path to a file or URL of the new catalog.  
![the Edit icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.edit.svg) or `Enter`| Use this icon or shortcut to change the added catalog or its path.  
![the Remove icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg) or `Alt+Delete`| Use this icon or shortcut to delete the added catalog.  
  
Item| Description  
---|---  
Name| The following catalog names can be applied: 

  * Internal: is the system catalog that is part the Maven distribution.
  * Default Local: is the catalog that is located in the `.m2` directory of your local machine.
  * Maven Central: is the catalog located at [Maven central repository](https://maven.apache.org/repository/).

  
Type| Type of a catalog. The System catalogs cannot be modified. If you add a custom catalog, it could be a Local catalog or a Remote one depending on the location of the specified catalog. Those catalogs can be modified or removed as needed.  
Location| Path to the location of the catalog.  
  
09 September 2024

[Maven. Repositories](maven-repositories.html)[Gradle settings](gradle-settings.html)
