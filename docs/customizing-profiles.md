[//]: # (Source: https://www.jetbrains.com/help/idea/customizing-profiles.html)
[//]: # (Downloaded: 2025-12-17 19:23:46)

## Move profiles between levels

In IntelliJ IDEA, inspection profiles can be stored at two levels:

  * Profiles Stored in IDE are saved to the inspection folder in the IntelliJ IDEA [configuration directory](directories-used-by-the-ide-to-store-settings-caches-plugins-and-logs.html#config-directory) and are accessible across all projects. While they cannot be shared via VCS, you can copy them to the project level to share them with your team.

  * Profiles Stored in Project are saved to the inspectionProfiles folder in the .idea directory and are specific to a single project. Unlike IDE-level profiles, project-level profiles can be shared with team members via VCS.




### Copy an IDE profile to the project level

You can copy an IDE profile to the project using the Copy to Project option. This allows you to share the profile via VCS or create a project-specific inspection profile.

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Inspections. 

  2. From the Profile drop-down list, select the profile you want to copy, then click ![the Show Scheme Actions](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) and select Copy to Project.

  3. Name the new profile and press `Enter` to save the changes.




After that, the new profile appears in the Commit tool window (`Alt+0`).

### Copy a project profile to the IDE level

You can copy a project profile to the IDE level using the Copy to IDE option. By doing so, you can use the profile in all projects that you work with in this IDE instance.

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Inspections. 

  2. From the Profile drop-down list, select the project profile you want to copy, then click ![the Show Scheme Actions](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) and select Copy to IDE.

  3. Name the new profile and press `Enter` to save the changes.




After that, the new profile becomes available in all projects that you open in the current IDE instance.
