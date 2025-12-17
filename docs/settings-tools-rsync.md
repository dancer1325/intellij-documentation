[//]: # (Source: https://www.jetbrains.com/help/idea/settings-tools-rsync.html)
[//]: # (Downloaded: 2025-12-17 20:02:06)

# Rsync

Use this page to configure the settings for [Rsync](https://rsync.samba.org), which facilitates download, upload, and synchronization of files in [a remote SFTP server configuration](creating-a-remote-server-configuration.html).

  * On macOS and Linux, the `rsync` and `ssh` tools are preinstalled and their paths are filled automatically.

  * On Windows, you need to manually install [Cygwin](https://www.cygwin.com) with the `rsync` and `openssh` packages first. The tools' executables are commonly located in the <Cygwin installation>\bin folder.




Rsync is used for [download and upload (including auto-upload) of files](uploading-and-downloading-files.html) and [synchronization](comparing-deployed-files-and-folders-with-their-local-versions.html) between the deployed files and folders and their local versions. Deletion and navigation by files on a remote host is still done via SFTP. 

Item| Description  
---|---  
Rsync executable path| In this field, provide the path to the `rsync` executable.  
Rsync options| Use this field to override the Rsync command-line parameters if necessary.By default, the `-zar` options are used, so that Rsync will compress the transferred data (`z`), preserve permissions, ownership, and timestamps of transferred files and folders (`a`), and recurse into subdirectories (`r`).For the complete list of available options, refer to the [Rsync documentation](https://linux.die.net/man/1/rsync).  
Shell executable path| In this field, provide the path to the `ssh` executable.  
Test Connection| Click this button to validate the provided settings and make sure that IntelliJ IDEA can properly communicate with Rsync.  
  
20 June 2025

[Remote external tools settings](settings-tools-remote-ssh-external-tools.html)[Settings Repository](settings-tools-settings-repository.html)
