[//]: # (Source: https://www.jetbrains.com/help/idea/share-code-with-gitlab-snippets.html)
[//]: # (Downloaded: 2025-12-17 20:02:32)

# Share code with GitLab snippets

Use [GitLab snippets](https://docs.gitlab.com/ee/user/snippets.html) to store and quickly share bits of code, files, or entire folders with others.

To use this feature, you should be logged in to your GitLab account or have at least one repository linked to a remote GitLab project.

### Create a snippet

  1. Select a code fragment in the editor, or files and folders you want to include to the new snippet in the Project tool window `Alt+1`.

Selecting a folder includes all files in it.

A single snippet can support [up to 10 files](https://docs.gitlab.com/ee/user/snippets.html#add-or-remove-multiple-files).

  2. Right-click the selection to open the context menu and then select Create Snippet.

The Create a GitLab Snippet dialog opens.

![A dialog with a list of options to create a GitLab snippet](https://resources.jetbrains.com/help/img/idea/2025.3/create_snippet_dialog.png)
  3. Specify the Project parameter:

     * If you want to create a project snippet, choose a project from the list of available GitLab projects you can create your snippet for.

To make this snippet listed under the chosen project, but visible only to you, keep the Private box checked.

     * If you want to create a personal snippet, choose None.

  4. Add a title and, optionally, a description of the new snippet.

  5. Specify the Path handling mode parameter to prevent duplication when passing the name of each file in the snippet to GitLab:

     * Relative: to find the nearest common parent of the selected files and pass along the paths to the files relative to that common parent.

     * Content root relative: to include the path of the files relative to the module.

     * Project relative: to include the path of the files relative to the project.

     * No paths: to pass along the filenames only, without a path.

Learn more about IntelliJ IDEA module system from [Content roots](content-roots.html).

  6. Select the Private checkbox to make this snippet visible only to you.

  7. Select the Copy URL checkbox to copy the link to the new snippet once it is created.

  8. Select the Open in browser checkbox to open the new snippet in [a default browser](settings-tools-web-browsers.html#defaultBrowser) once the snippet is created.

  9. Click OK.




28 November 2025

[Review incoming GitLab merge requests](work-with-gitlab-merge-requests.html)[GitLab CI/CD](gitlab-ci-cd.html)
