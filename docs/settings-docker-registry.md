[//]: # (Source: https://www.jetbrains.com/help/idea/settings-docker-registry.html)
[//]: # (Downloaded: 2025-12-17 20:00:53)

## Azure Container Registry

IntelliJ IDEA supports adding an [Azure Container Registry](https://learn.microsoft.com/en-us/azure/container-registry/) as a Docker V2 registry.

If you are using a temporary token for [individual login with Azure AD](https://learn.microsoft.com/en-us/azure/container-registry/container-registry-authentication?tabs=azure-cli#individual-login-with-azure-ad), set the username to `00000000-0000-0000-0000-000000000000` and the password to the token returned by `az acr login` with the `--expose-token` parameter. Use these commands to log in to the Azure CLI and expose the token:

az login az acr login --name <azureregistryname> \--expose-token 

When the temporary token expires, you will need to generate a new one and update it in the registry settings.

If you want to use an [admin user account](https://learn.microsoft.com/en-us/azure/container-registry/container-registry-authentication?tabs=azure-cli#admin-account), enable it in the Azure portal or via the Azure CLI:

az acr update -n <azureregistryname> \--admin-enabled true 

You can set the admin username and password when configuring your Azure Container Registry.
