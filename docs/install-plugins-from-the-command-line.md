[//]: # (Source: https://www.jetbrains.com/help/idea/install-plugins-from-the-command-line.html)
[//]: # (Downloaded: 2025-12-17 19:29:34)

# Install plugins from the command line

Install plugins by plugin ID from the [JetBrains Marketplace](https://plugins.jetbrains.com/) or a [custom plugin repository](managing-plugins.html#repos).

Installing plugins means putting them in the [plugins directory](directories-used-by-the-ide-to-store-settings-caches-plugins-and-logs.html#plugins-directory). If you run this command on a fresh IntelliJ IDEA installation, the IDE will not suggest importing the settings from the previous installation when you launch it for the first time, because the settings will no longer be empty.

You can find the executable for running IntelliJ IDEA in the installation directory under bin. To use this executable as the command-line launcher, add it to your system `PATH` as described in [Command-line interface](working-with-the-ide-features-from-command-line.html).

Syntax
    

idea64.exe installPlugins <plugin-id ...> [repository-url ...] 

Examples
    

Install the [GitHub plugin](https://plugins.jetbrains.com/plugin/13115-github/):

idea64.exe installPlugins org.jetbrains.plugins.github 

Install a plugin with the ID `com.example.myplugin` from a custom repository `http://plugins.example.com:8080/updatePlugins.xml`:

idea64.exe installPlugins com.example.myplugin http://plugins.example.com:8080/updatePlugins.xml 

By default, IntelliJ IDEA does not provide a command-line launcher. For more information about creating a launcher script for IntelliJ IDEA, refer to [Command-line interface](working-with-the-ide-features-from-command-line.html).

Syntax
    

idea installPlugins <plugin-id ...> [repository-url ...] 

Examples
    

Install the [GitHub plugin](https://plugins.jetbrains.com/plugin/13115-github/):

idea installPlugins org.jetbrains.plugins.github 

Install a plugin with the ID `com.example.myplugin` from a custom repository `http://plugins.example.com:8080/updatePlugins.xml`:

idea installPlugins com.example.myplugin http://plugins.example.com:8080/updatePlugins.xml 

You can find the script for running IntelliJ IDEA in the installation directory under bin. To use this script as the command-line launcher, add it to your system `PATH` as described in [Command-line interface](working-with-the-ide-features-from-command-line.html).

Syntax
    

idea.sh installPlugins <plugin-id ...> [repository-url ...] 

Examples
    

Install the [GitHub](https://plugins.jetbrains.com/plugin/13115-github/) plugin:

idea.sh installPlugins org.jetbrains.plugins.github 

Install a plugin with the ID `com.example.myplugin` from a custom repository `http://plugins.example.com:8080/updatePlugins.xml`:

idea.sh installPlugins com.example.myplugin http://plugins.example.com:8080/updatePlugins.xml 

If the plugin is distributed as a JAR archive, copy the JAR file to the [plugins directory](directories-used-by-the-ide-to-store-settings-caches-plugins-and-logs.html#plugins-directory) and restart the IDE:

copy plugin.jar %APPDATA%\JetBrains\Roaming\<Product><Version>\plugins\ 

cp plugin.jar ~/Library/Application Support/JetBrains/<Product><Version>/plugins/ 

cp plugin.jar ~/.local/share/JetBrains/<Product><Version>/plugins/ 

The developer of the plugin specifies a unique identifier for the plugin in plugin.xml – the [plugin configuration file](https://plugins.jetbrains.com/docs/intellij/plugin-configuration-file.html#idea-plugin__id). If it is a public plugin, you can find its ID on the page of the plugin in JetBrains Marketplace. Scroll down to the Additional Information section and copy the value from the Plugin ID parameter.

![Plugin ID](https://resources.jetbrains.com/help/img/idea/2025.3/pluginID.png)

11 November 2025

[Run code inspections from the command line](command-line-code-inspector.html)[Tutorial: Build UI using Swing](design-gui-using-swing.html)
