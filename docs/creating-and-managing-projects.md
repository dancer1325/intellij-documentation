[//]: # (Source: https://www.jetbrains.com/help/idea/creating-and-managing-projects.html)
[//]: # (Downloaded: 2025-12-17 19:23:19)

## Project formats

In IntelliJ IDEA, there are two types of formats in which a project's configuration can be stored — the file-based format and the directory-based format.

### File-based format

The file-based format was the only one available in older versions of IntelliJ IDEA; now it is outdated. Projects in this format contain several files: the .ipr, .iws, and .iml files. Generally, we don't recommend using this format unless you need to open projects in different file managers by clicking the .ipr file, or unless you need to store multiple projects in one directory.

![A simple file-based project shown in Finder](https://resources.jetbrains.com/help/img/idea/2025.3/file-based-in-finder.png)

### Directory-based format

For the directory-based format, the IDE creates the .iml file and the .idea directory that keeps project settings. It's the default format for projects in IntelliJ IDEA at this moment.

This format was introduced after the file-based format. Its main advantage is that it's adjusted to store project files in Version Control Systems: the project data is split over multiple files, and merge conflicts are less likely. For more information about sharing projects in different formats, refer to [How to manage projects under Version Control Systems](https://intellij-support.jetbrains.com/hc/en-us/articles/206544839)

On macOS and Linux, the .idea directory is hidden by default. To display the directory, allow showing hidden files in your system settings.

![A simple directory-based project shown in Finder](https://resources.jetbrains.com/help/img/idea/2025.3/project-in-finder.png)

### Change the project format to directory-based

  1. Open the project using the .ipr file: go to File | Open in the main menu and select the .ipr in the folder with the project that you want to convert.

  2. When the project has opened, in the main menu, go to File | Manage IDE Settings | Save as Directory-Based Format.



