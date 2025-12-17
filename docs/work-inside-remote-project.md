[//]: # (Source: https://www.jetbrains.com/help/idea/work-inside-remote-project.html)
[//]: # (Downloaded: 2025-12-17 20:07:01)

## Install plugins

You can install plugins that you need for your remote projects.

Based on the scenario that you use for downloading IntelliJ IDEA on the remote server, you either install the plugin via the command line or use the UI of a remote project for your installation.

When you install a plugin, an indicator appears on the [Plugins settings](plugins-settings.html) description page showing where the plugin is installed — on the remote host, on the JetBrains client, or on both.

![The Plugins settings dialog](https://resources.jetbrains.com/help/img/idea/2025.3/settings_remote_plugins.png)

Note that plugins are installed per project. Each time you create a remote connection for a new project, you need to install the required plugin.

If you encounter a problem with the plugin you are trying to install, submit an issue to our [support team](https://www.jetbrains.com/support/).

### Install a plugin through the command line

If you [manually configure](remote-development-a.html#use_idea) IntelliJ IDEA on the remote server, use the following steps to add plugins:

  1. In [JetBrains Marketplace](https://plugins.jetbrains.com/), find a page of the plugin that you want to install, scroll down to the Additional Information section, and copy the value from the Plugin ID parameter, for example, `org.jetbrains.plugins.github`.

  2. Open the remote server, go to the IntelliJ IDEA instance where your project resides, and for which you want to download and install a third-party plugin.

By default, the downloaded IntelliJ IDEA instances are located in the following directory:

~/.cache/JetBrains/RemoteDev/dist 

  3. Add the following command: 

bin/remote-dev-server.sh installPlugins PROJECT_PATH pluginId 

(where `PROJECT_PATH` is a path to your remote project and `pluginId` is an ID you got from [JetBrains Marketplace](https://plugins.jetbrains.com/) page.)

If the backend is started with a third-party plugin that isn't enabled, the plugin will be disabled, and a message will appear in the log suggesting that users use the `--give-consent-to-use-third-party-plugins` option with `installPlugins`.

After the installation, unpack the downloaded plugin's archive.

By default, the installed plugin is placed into the following folder on the backend:

~/.local/shared/JetBrains/<ide name><ide version>

  4. Continue with [launching JetBrains Gateway](remote-development-a.html#use_local_ide) and opening the remote project with the remotely installed plugin.




### Install a plugin via UI

If you [use JetBrains Gateway](remote-development-a.html#launch_gateway) to download IntelliJ IDEA to a remote server, use the following steps to install plugins.

  1. Open a remote project in the JetBrains Client.

  2. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  3. [Install](managing-plugins.html#install_plugin_from_repo) the necessary plugin the same way as you would in a regular IntelliJ IDEA project.

![The Plugins settings dialog](https://resources.jetbrains.com/help/img/idea/2025.3/plugins_remote.png)

For more information about regular plugin installation, refer to [Install plugins](managing-plugins.html).

  4. After you download and enable the plugin, click OK to save the changes.

The plugin is installed remotely. However, keep in mind that the plugin is installed per project.

When you use the `gateway installPlugins *idPlugin*` command to install plugins before starting JetBrains Gateway, third-party plugins will not be downloaded automatically upon JetBrains Gateway start. Instead, you will receive a message prompting you to accept the installation of third-party plugins.

To bypass this message and install the necessary third-party plugins at Gateway's startup, use the following command:

`gateway installPlugins *idPlugin* --give-consent-to-use-third-party-plugins`



