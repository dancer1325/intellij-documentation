[//]: # (Source: https://www.jetbrains.com/help/idea/flyway.html)
[//]: # (Downloaded: 2025-12-17 19:27:11)

## Flyway Versioned Migration Preview Window

![flyway-preview](https://resources.jetbrains.com/help/img/idea/2025.3/flyway_versioned_migration_preview.png)

IntelliJ IDEA allows you to select the place where to store the generated script: you can choose a file, scratch file in the IDE or clipboard.

Directory and File name fields are responsible for configuring the location of the generated migration. If a migration with the specified name already exists, you will be prompted with a warning, after which the changes will be appended to that migration.

On the left of the window, there is a preview of the actual changes to be generated. You can see what each change is going to look like by clicking on them.

Above the list of changes, you can use the following buttons:

![](https://resources.jetbrains.com/help/img/idea/2025.3/jpa-model.icons.newui.addChangelog.svg)
    

Add Versioned Migration

Create a secondary versioned migration.

![](https://resources.jetbrains.com/help/img/idea/2025.3/jpa-model.icons.newui.removeDropDown.svg)
    

Remove from Versioned Migration

Remove the changes and add them to the Ignored section, so they are excluded from future migrations.

![](https://resources.jetbrains.com/help/img/idea/2025.3/jpa-model.icons.newui.restoreFromIgnore.svg)
    

Restore from Ignored

Move the changes from Ignored to the migration.

![](https://resources.jetbrains.com/help/img/idea/2025.3/jpa-model.icons.newui.moveToAnotherChangelog.svg)
    

Move to Another Versioned Migration

By default, a single migration script is created on each diff generation with all the changes. This action lets you move a change to another migration file.

![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.inline.inlineSettings.svg)
    

Show Other Actions

Interact with a large number of changes in the migration files: Select all, Expand all, and Collapse all.

To combine several changes into one migration file or to ignore them, drag them around.
