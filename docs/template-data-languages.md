[//]: # (Source: https://www.jetbrains.com/help/idea/template-data-languages.html)
[//]: # (Downloaded: 2025-12-17 20:04:04)

## Fixing unresolved references

IntelliJ IDEA provides [inspections](code-inspection.html) for detecting unresolved references in template languages:

![Example template language inspection for unresolved references](https://resources.jetbrains.com/help/img/idea/2025.3/velocity_inspection.png)

Unresolved references can be fixed using [intention actions](intention-actions.html). You can select to add a comment in the same file, or to create a separate file with comments. For more information, refer to [Special comments](#special-comments).

![Example template language intentions for fixing unresolved references](https://resources.jetbrains.com/help/img/idea/2025.3/velocity_intention.png)

Comments in such cases are used to provide missing info about the references.

In the latter case, a file with the default name `velocity_implicit.vm` or `freemarker_implicit.ftl` is created. This file starts with the following comment:

#* @implicitly included *#

Code completion for defining reference types is available in the comments files.

If you rename the file or move it to a different location within the source root, reference definitions will not be lost.
