[//]: # (Source: https://www.jetbrains.com/help/idea/default-permissions.html)
[//]: # (Downloaded: 2025-12-17 19:24:31)

# Files/Folders Default Permissions dialog

This dialog opens when you select the Override default permissions on files or Override default permissions on folders checkbox in the [Options](settings-deployment-options.html) dialog and click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.inline.browse.svg) next to it.

![Override default permissions on files](https://resources.jetbrains.com/help/img/idea/2025.3/override_default_permissions_on_files.png)

Use this dialog to re-assign default server permissions to owners of files or folders, groups of owners, and other users.

  * R stands for Read.

  * W stands for Write.

  * X stands for Execute




Item| Description  
---|---  
Owner| In this row, specify what an owner of a file or folder may do by selecting the checkboxes below the corresponding identifiers.  
Group| In this row, specify what a group of owners of a file or folder may do by selecting the checkboxes below the corresponding identifiers.  
Others| In this row, specify what anyone else may do by selecting the checkboxes below the corresponding identifiers.  
Octal| In this field, specify the [octal representation](http://www.slackbook.org/html/filesystem-structure-permissions.html) of the specified set of permissions. By default, IntelliJ IDEA calculates and re-calculates the value of the field as you select or clear the desired checkboxes. You can also specify the octal value manually.  
  
17 June 2024

[Options](settings-deployment-options.html)[Docker connection settings](settings-docker.html)
