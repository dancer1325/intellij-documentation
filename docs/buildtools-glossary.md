[//]: # (Source: https://www.jetbrains.com/help/idea/buildtools-glossary.html)
[//]: # (Downloaded: 2025-12-17 19:19:35)

# Build tools glossary

The following table is intended for the internal use and covers all the terms used in the build tools documentation and the UI.

Term| Description  
---|---  
Import (deprecated)| A process of opening, loading a project into the IDE, executing code from its build scripts, and synchronizing the project's dependencies.  
Open| A process of opening a project, loading a project into the IDE and synchronizing its dependencies.  
Sync (deprecated)| A process of synchronizing all linked projects and their dependencies after opening the main project inside the IDE.  
Build| A process of compiling all the classes inside a build target (module or a project) and placing them inside the output directory.  
Rebuild| When a rebuild command is executed, IntelliJ IDEA cleans out the entire output directory, deletes the build caches and builds a project, or a module from scratch.  
Auto-build| A process of automatic incremental compilation of a project, every time the changes are made to it.  
Load| A process of synchronizing changes made to a build script file.  
Reload| A process of re-importing all the linked projects.  
Auto-Reload| An automatic process of adding changes made in a build script file and re-importing the project.  
Link| Attaching another project to the existing one.  
Unlink| A process of removing all relevant modules and content roots, removing of the project from the appropriate build tools' tool window and stopping its synchronization.  
Remove|   
Ignore| A process of deactivating a project. In this case, IntelliJ IDEA keeps the ignored projects and subprojects in the appropriate build tools' tool window, but stops their import (modules, content roots, tasks, and so on) to the project. However, IntelliJ IDEA synchronizes the ignored projects with the current one.  
Task| A piece of work that Gradle performs as a part of its build cycle.  
Goal| A piece of work that Maven performs as a part of its Lifecycle.  
Target| A piece of work that Ant performs as a part of its build cycle.  
  
11 February 2024

[Package Search](package-search.html)[Java bytecode decompiler](decompiler.html)
