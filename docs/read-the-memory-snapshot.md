[//]: # (Source: https://www.jetbrains.com/help/idea/read-the-memory-snapshot.html)
[//]: # (Downloaded: 2025-12-17 19:56:47)

## Object view

The Object view displays class instances ordered by their retained size.

You can open the view by double-clicking an item on the Classes tab. You can also right-click an item and select Open in New Tab or press `Enter`.

![A class shown in the Object view of the Profiler tool window](https://resources.jetbrains.com/help/img/idea/2025.3/hprof-object-view.png)

For each class instance, there are several tabs that allow you to calculate and display the following information:

  * Shortest Paths: the shortest reference chains to garbage collector roots.

  * Incoming References: incoming references from other instances.

  * Dominators: allows you to see what objects retain particular instances (prevent them from being garbage collected). Every instance has only one dominator or hasn't got any.

  * Retained Objects: a sunburst diagram showing how retained objects contribute to the retained size of a particular object.

  * Dominator Tree: the tree of retained objects. It allows you to see how much memory can be reclaimed by removing a reference to a specific object and which particular objects will be garbage-collected together with it.



