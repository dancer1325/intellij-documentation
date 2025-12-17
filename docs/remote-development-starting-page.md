[//]: # (Source: https://www.jetbrains.com/help/idea/remote-development-starting-page.html)
[//]: # (Downloaded: 2025-12-17 19:57:12)

## Connection via SSH

The connection to a remote server is done via SSH and can be started right from the welcome screen of IntelliJ IDEA.

On how to access the welcome screen, refer to [Installation guide](installation-guide.html).

![IntelliJ IDEA welcome screen](https://resources.jetbrains.com/help/img/idea/2025.3/idea_remote_development.png)

### Connect to a remote server and open the remote project

  1. Ensure you have the [Remote Development Gateway plugin enabled](jetbrains-gateway.html#plugin_install).

  2. On the IntelliJ IDEA welcome screen, select Remote Development. Alternatively, go to File | Remote Development in the main menu.

  3. Under SSH Connection, click New Connection.

If you have the IDE already running on the remote server, and you have a [connection link](remote-development-a.html#use_idea), you can use the Connect to Running IDE section.

  4. Configure the [remote server connection parameters](remote-development-a.html#configure_server_parameters) and click Check Connection and Continue to make sure the connection to the remote server is successful.

![IntelliJ IDEA welcome screen](https://resources.jetbrains.com/help/img/idea/2025.3/connect_to_ssh.png)
  5. On the next page of the wizard, in the IDE version field, select the source of the remote IDE that you want to use.

Use one of the following ways to get an IDE installer:

     * Automatically fetch from JetBrains installers storage - default variant.

Your remote server must have a network connection to JetBrains URLs:

https://code-with-me.jetbrains.com https://download.jetbrains.com https://download-cf.jetbrains.com https://cache-redirector.jetbrains.com 

     * Fetch from your company's internal storage. In this case, you need to click Other options and select Use download link. It is helpful if remote machines do not have an Internet connection to JetBrains' websites or your organization uses some custom builds.

     * Upload from your local machine. In this case, click Other options and select Upload installer file. You need to get the IDE `.tar.gz` archive from the JetBrains website by yourself in advance.

Since IntelliJ IDEA versions 2022.1+, you can also select a custom path on the remote side for the unpacked backend installer. Use this option if a default directory does not have enough space.

![IntelliJ IDEA welcome screen](https://resources.jetbrains.com/help/img/idea/2025.3/ide_version_field.png)
  6. Click Start IDE and Connect.

IntelliJ IDEA starts JetBrains Gateway, which downloads the IDE backend, launches, and opens [JetBrains Client](remote-development-overview.html#thin_client) with your [remote project](work-inside-remote-project.html).




For more information about starting to work with a separate JetBrains Gateway installer, refer to [JetBrains Gateway](remote-development-a.html#gateway).

For more information about adding plugins or SDK, refer to the appropriate [Getting Started](work-inside-remote-project.html#plugins) section.
