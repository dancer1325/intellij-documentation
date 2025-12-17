[//]: # (Source: https://www.jetbrains.com/help/idea/contexts.html)
[//]: # (Downloaded: 2025-12-17 19:22:28)

# Contexts

A context is a set of bookmarks, breakpoints, and tabs opened in the editor. Contexts are linked to tasks, but you can work with contexts without associating them with specific tasks.

Having separate contexts lets you work on several things and switch between them without mixing the changes.

You can view the list of bookmarks and breakpoints in the [Bookmarks](bookmarks.html) tool window.

### Save a context

  1. In the main menu, go to Tools | Tasks & Contexts | Save Context.

  2. In the Save Context dialog, enter the name of the context and click OK.




### Modify existing contexts

To modify an existing context, start by loading it. Once it is loaded, you can add or remove items as needed, then save the updated version.

  1. In the main menu, go to Tools | Tasks & Contexts | Load Context.

  2. Add bookmarks or breakpoints or open the necessary files and save the context: in the main menu, go to Tools | Tasks & Contexts and select Save Context.




### Switch between contexts

When you switch tasks, the IDE automatically updates the related contexts. However, if your contexts aren't linked to tasks, you can switch between them manually.

  1. In the main menu, go to Tools | Tasks & Contexts | Load Context.

  2. In the Load Context popup, select the necessary context from the list.

Alternatively, click the right arrow and select Load.

![Loading a context](https://resources.jetbrains.com/help/img/idea/2025.3/load-contexts-popup.png)



### Clear a context

  * To clear the current context without loading another one, select Tools | Tasks & Contexts | Clear Context from the main menu or press `Alt+Shift+X`.




### Delete a context

When a task is finished, or if you do not need a context anymore, you can remove it.

  1. In the main menu, go to Tools | Tasks & Contexts | Load Context.

  2. In the Load Context popup, click the right arrow and select Remove.




02 November 2024

[Tutorial: Configure a generic task server](tutorial-configuring-generic-task-server.html)[Command-line interface](working-with-the-ide-features-from-command-line.html)
