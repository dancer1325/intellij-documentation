[//]: # (Source: https://www.jetbrains.com/help/idea/tagging-changesets.html)
[//]: # (Downloaded: 2025-12-17 20:03:56)

# Tag changesets and repositories

IntelliJ IDEA supports both local and global tags. Local tags are stored in the file .hg/localtags in the repository, global tags are stored in the file .hgtags.

Currently, tagging specific changesets is supported only in the command line mode in the [embedded Terminal](terminal-emulator.html). To launch the Terminal, hover over ![the Tool windows icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.tbHidden.svg) in the lower left corner of the IDE, then choose Terminal from the menu. After commit, tags appear in the Log tab of the Mercurial tool window `Alt+9`.

For more information about Mercurial tags, refer to [Mercurial Documentation: Tag](https://www.mercurial-scm.org/wiki/Tag).

### Tag a repository

IntelliJ IDEA provides UI for tagging the current repository which means assigning a tag to its tip. The created tag is global, is stored in the file .hgtags. After commit, the tag appears in the Log tab of the Mercurial tool window `Alt+9`.

  1. Open the Tag dialog by doing one of the following:

     * Go to VCS | Mercurial | Tag Repository.

     * From the context menu of the Editor, choose Mercurial | Tag Repository.

  2. In the Tag dialog that opens, specify the tag name. The name must be unique.




11 February 2024

[Manage Mercurial branches and bookmarks](managing-mercurial-branches-and-bookmarks.html)[Switch between Mercurial working directories](switching-between-working-directories.html)
