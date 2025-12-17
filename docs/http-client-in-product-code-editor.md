[//]: # (Source: https://www.jetbrains.com/help/idea/http-client-in-product-code-editor.html)
[//]: # (Downloaded: 2025-12-17 19:29:00)

## Create HTTP request files

You can work with HTTP requests either from scratch files or from physical files of the HTTP Request type. Each file can contain multiple requests, and you can create as many files as needed.

[Scratch files](scratches.html) can be used to test HTTP requests during development. Scratch files are not stored inside a project, so IntelliJ IDEA can modify them and add additional information about the request. When an HTTP request is executed from a scratch file, the link to the response output file is added below the request and at the top of the [requests history](#requests_history) file.

### Create an HTTP request scratch file

  * Press `Ctrl+Alt+Shift+Insert` and select HTTP Request.




Physical files can be used for documenting, testing, and validating HTTP requests. Physical files are stored inside your project, and IntelliJ IDEA will not modify them. When an HTTP request is executed from a physical file, this file is not modified. Information about the executed request with the link to the response output file is added to the top of the [requests history](#requests_history) file.

### Create a physical HTTP request file

  * In the File menu, point to New, and then click HTTP Request. 




### Move an HTTP request

You can use the [Move](move-refactorings.html) refactoring `F6` to move HTTP requests from scratches to physical files, as well as between physical files.

  1. In the editor, place the caret at the request to be moved and do one of the following:

     * From the main menu or the context menu, select Refactor | Move.

     * Press `Alt+Enter` and select the Move HTTP Requests [intention action](intention-actions.html).

     * Press `F6`.

  2. In the Move HTTP Requests dialog that opens, do the following:

     1. In the Path field, choose one of the existing .http files from the list or click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) to locate the file.

You can also type the full path to the file manually. If you specify the name of a non-existing file, a new file with the provided name will be created automatically.

     2. In the Requests list, select the checkboxes next to the requests you want to move.



