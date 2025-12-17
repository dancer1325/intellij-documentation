[//]: # (Source: https://www.jetbrains.com/help/idea/fully-offline-mode.html)
[//]: # (Downloaded: 2025-12-17 19:27:21)

## Configure the version management of JetBrains Client

In some cases, you might need to control local JetBrains Client versions.

For that purpose, you need to set a value for the `versionManagementEnabled` parameter in OS registry named `OsRegistryConfigProvider`. The location of the registry depends on your OS.

For the whole system:

/Library/Application Support/JetBrains/JetBrainsClient/config.json

For a specific user:

~/Library/Application Support/JetBrains/JetBrainsClient/config.json

Write a json object with a parameter `versionManagementEnabled` and a value `"true"`.

If you want this parameter disabled, add `"false"` instead of `"true"`.

Example of the `json` file:

{ "versionManagementEnabled": "true" } 

Alternatively, you can create a separate config file with the name `versionManagementEnabled` and the value `false` inside to disable the automatic management.

For the whole system:

/etc/xdg/JetBrains/JetBrainsClient/config.json

For a specific user:

~/.config/JetBrains/JetBrainsClient/config.json

or other XDG_CONFIG_HOME if specified: https://specifications.freedesktop.org/basedir-spec/basedir-spec-0.6.html

Write a json object with a parameter `versionManagementEnabled` and a value `"true"`.

{ "versionManagementEnabled": "true" } 

If you want this parameter disabled, add `"false"` instead of `"true"`.

Alternatively, you can create a separate config file with the name `versionManagementEnabled` and the value `false` inside to disable the automatic management.

For the whole system:

HKEY_LOCAL_MACHINE/SOFTWARE/JetBrains/JetBrainsClient

For a specific user:

HKEY_CURRENT_USER/SOFTWARE/JetBrains/JetBrainsClient

Create `REG_SZ` or `REG_EXPAND_SZ` entry with `versionManagementEnabled` as the key and `true` as a value.
