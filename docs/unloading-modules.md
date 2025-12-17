[//]: # (Source: https://www.jetbrains.com/help/idea/unloading-modules.html)
[//]: # (Downloaded: 2025-12-17 20:05:02)

## Automatically load and unload new modules

If your teammates add new modules to a project, you will download them to your computer on the project update. After that, the IDE will analyze the dependencies between all modules in the updated project.

If you have unloaded modules, IntelliJ IDEA will load or unload new modules according to the results of the dependency analysis.

If new modules depend on the existing unloaded modules, the new modules will be marked as unloaded. IntelliJ IDEA will ignore them because otherwise you may face errors when you try to compile them.

![Adding new modules to the unloaded module](https://resources.jetbrains.com/help/img/idea/2025.3/projects_unloaded_new_unloaded.png)

If existing loaded modules have direct dependencies on new modules, the new modules will be marked as loaded.

![Adding new modules to the loaded module](https://resources.jetbrains.com/help/img/idea/2025.3/projects_unloaded_new_loaded.png)

If existing loaded modules have no dependencies on the newly added modules, the new modules will be marked as unloaded. You can manually mark them as loaded as soon as you need them.

![Adding new modules to the loaded module with no dependencies](https://resources.jetbrains.com/help/img/idea/2025.3/projects_unloaded_new.png)
