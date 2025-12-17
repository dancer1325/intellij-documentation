[//]: # (Source: https://www.jetbrains.com/help/idea/exporting-information-from-subversion-repository.html)
[//]: # (Downloaded: 2025-12-17 19:26:09)

# Export information from Subversion repository

You might need to obtain a _clean_ local copy of the Subversion working tree without the .svn catalogs. Instead of checking files out and then manually deleting the administrative directories, you can use the Export command available in the Subversion repository browser.

To export a directory from a Subversion repository, do the following:

  1. In the main menu, go to VCS | Browse VCS Repository | Browse Subversion Repository to open the [SVN Repositories](svn-repositories.html) tool window.

  2. Right-click a directory you want to export and choose Export from the context menu.

  3. In the Select Path dialog that opens, specify the destination directory and click OK.

  4. In the SVN Export Options dialog that opens, check the Export and Destination paths and specify the following options:

     * Depth: use this list to specify the range of recursion into Subversion subdirectories. The available options are: 

       * working copy: select this option to get files/directories from the repository subtrees that have not been checked out yet.

       * empty: select this option to involve only the current file.

       * files: select this option to involve files from the current folder.

       * immediates: select this option to involve direct children of the current file.

       * infinity: select this option to enable full recursion.

     * Replace existing files: select this option to replace files in the destination directory with the exported sources.

     * Include external locations: select this option to include external references into the export.

     * Override 'native' EOLs with:: use this list if you want to override the `svn:eol-style=native` property. This is useful if team members sharing the same repository use different operating systems, which may result in problems with line endings. The following options for line separators are available:

       * None: this option is selected by default, and keeps the `svn:eol-style=native` property unchanged.

       * LF: select this option if you are using unix

       * CRLF: select this option if you are using Windows

       * CR: select this option if you are using macOS




11 February 2024

[Create Subversion branches and tags](creating-branches-and-tags.html)[Import a local directory to Subversion repository](importing-a-local-directory-to-subversion-repository.html)
