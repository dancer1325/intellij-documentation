[//]: # (Source: https://www.jetbrains.com/help/idea/migrate.html)
[//]: # (Downloaded: 2025-12-17 19:32:28)

# Migrate

The Migrate refactoring lets you easily switch between the old packages and classes used in your project and the new ones. IntelliJ IDEA comes with a set of predefined migration maps.

This refactoring is also available from [UML Class diagram](class-diagram.html).

### Run the migration refactoring

  1. In the main menu, go to Refactor | Migrate Packages and Classes.

  2. Select the desired migration map from the list.

  3. In the dialog that opens, select the scope of file in which you want to refactor your code and click Run. 

![Running the migration refactoring](https://resources.jetbrains.com/help/img/idea/2025.3/migrate_refactoring.png)



### Create a new migration

  1. In the main menu, go to Refactor | Migrate Packages and Classes and click Create New Migration.

  2. Specify the name of the map and an optional map description.

  3. Click the ![Add](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) icon to create a new migration rule.

  4. In the dialog that opens, select whether you want to migrate packages or classes and specify the old and the new names of the package or class. Click OK.

  5. Create or edit as many migration rules as required. Use the ![Edit](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.edit.svg) button to edit the exiting rules.

  6. Click Save. After than, you can [run it from the main menu](#run_migration_refactoring).




### Edit an existing migration map

You can edit a migration map that you have created previously. If you want to modify a predefined map, create its copy first and then change the map as necessary.

  1. Go to Refactor | Migrate Packages and Classes and click the migration map that you want to edit.

If you are modifying a predefined map, click Duplicate and edit.

  2. In the dialog that opens, select Edit and modify the existing migration rules.

  3. Click Save. After than, you can [run it from the main menu](#run_migration_refactoring).




### Share a migration map

  1. Go to the IntelliJ IDEA [configuration directory](directories-used-by-the-ide-to-store-settings-caches-plugins-and-logs.html#config-directory).

  2. Find the migration directory and locate the relevant migration map  .xml file you want to share.




11 October 2024

[Make Static](make-method-static.html)[Move and copy refactorings](move-refactorings.html)
