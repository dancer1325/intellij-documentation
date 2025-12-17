[//]: # (Source: https://www.jetbrains.com/help/idea/customizing-devcontainer-json-file.html)
[//]: # (Downloaded: 2025-12-17 19:23:44)

## Customizing devcontainer.json file

You can customize `devcontainer.json` file by adding the required settings, plugins, and so on.

### Add modified settings

  1. Open the `devcontainer.json` file in the editor.

  2. In the left gutter, click ![Create Dev Container](https://resources.jetbrains.com/help/img/idea/2025.3/clouds-docker-gateway.icons.devContainers.svg), select Add Modified Settings from IDE. 

The settings are added as a `customizations` section. It might be useful if you want to synchronize both settings or choose some other customization option.

![JSON file customizations section](https://resources.jetbrains.com/help/img/idea/2025.3/customization_section.png)

You can also add the non-default application-level settings, modify the added settings options, sort them, or add properties from the JSON schema. Press `Alt+Enter` in the `settings` section of the `devcontainer.json` file and select the appropriate option.

![JSON settings](https://resources.jetbrains.com/help/img/idea/2025.3/json_settings.png)



You can also install plugins from the [JetBrains marketplace](https://plugins.jetbrains.com/) to a Dev Container.

### Add plugins

  1. Open [JetBrains marketplace](https://plugins.jetbrains.com/) in the browser.

  2. Locate the required plugin and open the plugin page.

  3. On the plugin page, scroll down to the Additional information section and copy plugin ID.

  4. Open the `devcontainer.json` file in the editor.

  5. Inside the `customizations` section, add the following code: 

{ "customizations": { "jetbrains": { "plugins": [ "org.intellij.plugins.hcl" ] } } } 

The `pluginID` is the ID of the required plugin from [JetBrains marketplace](https://plugins.jetbrains.com/), for example, `org.intellij.plugins.hcl`.



