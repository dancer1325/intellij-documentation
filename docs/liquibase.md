[//]: # (Source: https://www.jetbrains.com/help/idea/liquibase.html)
[//]: # (Downloaded: 2025-12-17 19:31:27)

## Changelog Preview Window

![changelog-preview](https://resources.jetbrains.com/help/img/idea/2025.3/changelog-preview.png)

If you want to save the changelog as a regular file, then the following configuration options will be available:

  * Directory and File name fields are responsible for configuring the location of the generated changelog. If a changelog with the specified name already exists, you will be prompted with a warning, after which the changes will be appended to that changelog.

  * You can use Include to, Include folder, and Include context to specify whether a changelog should be included in another changelog. If you check the Include folder box, it generates the include statement for the entire folder, not just the current changelog.

  * From the File type drop-down list, you can choose one of the four file types (YAML, JSON, SQL, XML) supported by Liquibase, in which IntelliJ IDEA will generate the changelog.




If you want to save the changelog as a scratch file, then you can configure only its name and type.

![liquibase-preview-scratch](https://resources.jetbrains.com/help/img/idea/2025.3/liquibase-preview-scratch.png)

The left side of the window shows a preview of the changesets that will be generated. You can click on each change to see what it will look like. To combine several changes into one changeset or to ignore them, simply drag and drop them. The top left corner of the preview window contains various actions to modify the resulting changelog:

![add-changelog-action](https://resources.jetbrains.com/help/img/idea/2025.3/add-changelog-action.jpeg)

The following actions are provided:

  * Add Changelog — create a secondary changelog

  * Add Change Set — create a new changeset in the selected changelog

  * Remove from Changelog with options: 

    * Remove from Changelog — simply remove the changes from the current changelog

    * Remove and Ignore — remove the changes and add them to Ignored, so they are excluded from future changesets too

    * Restore from Ignored — move the changes from Ignored to the changelog

  * Set Context (for changesets)

  * Set Labels (for changesets)

  * Show Other Actions — select all changes based on the danger level, expand/collapse all changes



