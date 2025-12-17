[//]: # (Source: https://www.jetbrains.com/help/idea/mcp-server.html)
[//]: # (Downloaded: 2025-12-17 19:32:17)

## External client setup

For external clients like Claude Code, Claude Desktop, Cursor, VS Code, Codex, and Windsurf, configuration can be performed automatically:

  1. In the main menu, go to Settings | Tools | MCP Server.

  2. Click Enable MCP Server.

  3. In the Clients Auto-Configuration section, click Auto-Configure for each client you want to set up for use with the MCP server. This will automatically update their JSON configuration.

![MCP Server settings](https://resources.jetbrains.com/help/img/idea/2025.3/ai_mcp_server_settings.png)

To check if the configuration was updated, click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.chevronDownLarge.svg), then select the Open Client Settings File option. This will open the client's JSON configuration file in the editor.

![Configuration options](https://resources.jetbrains.com/help/img/idea/2025.3/ai_mcp_server_config_options.png)

You can also copy the configuration to clipboard if you want to perform update manually by clicking Copy Config.

  4. Restart your client for configuration to take effect.




If you want to connect to the MCP server from any other client, you will need to perform manual configuration:

  1. In the Manual Client Configuration section, click either Copy SSE Config or Copy Stdio Config depending on the connection type.

![MCP Server manual configuration](https://resources.jetbrains.com/help/img/idea/2025.3/ai_mcp_server_manual_config.png)
  2. Paste the copied configuration into your client's settings or configuration file.

  3. Restart your client for configuration to take effect.



