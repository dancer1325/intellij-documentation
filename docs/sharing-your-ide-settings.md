[//]: # (Source: https://www.jetbrains.com/help/idea/sharing-your-ide-settings.html)
[//]: # (Downloaded: 2025-12-17 20:02:39)

## Share settings via the Backup and Sync plugin

### Enable the Backup and Sync plugin

This functionality relies on the [Backup and Sync](https://plugins.jetbrains.com/plugin/20868) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the Backup and Sync plugin, and select the checkbox next to the plugin name.




### Enable settings backup and synchronization

  1. On the computer with the IDE instance that contains the settings you want to share, sign in to either of the following:

     * Your IDE: from the main menu choose Help | Register, choose to activate your license with the [JetBrains Account](https://sales.jetbrains.com/hc/en-gb/articles/208459005-What-is-JetBrains-Account-) and enter your credentials.

     * [Toolbox App](https://www.jetbrains.com/toolbox/app/): click the gear icon ![toolbox settings](https://resources.jetbrains.com/help/img/idea/2025.3/toolboox_app_gear_icon.png) in the top right corner of the application, select Settings and click Log in. Note that by signing in to Toolbox App, you automatically sign in to all JetBrains products that you run.

     * If, instead of the JetBrains account, you use an activation code or a license server [to activate IntelliJ IDEA](register.html#activate-license), press `Ctrl+Alt+S` to open settings and select Backup and Sync | Log in with JetBrains account to sign in to your JetBrains account.

  2. Press `Ctrl+Alt+S` to open Settings, go to Backup and Sync, and then click Enable Backup and Sync.

  3. In the Backup and Sync dialog that opens, select the [setting categories](#settings-synchronized-by-settings-sync) that you want to share and if you want to share them across IntelliJ IDEA instances only or across all JetBrains IDEs.

  4. The following step depends on whether there are settings linked to your [JetBrains Account](https://sales.jetbrains.com/hc/en-gb/articles/208459005-What-is-JetBrains-Account-).

![The Settings Sync window](https://resources.jetbrains.com/help/img/idea/2025.3/settings_sync_list.png)

Click Push Settings to Account to override the settings stored on the JetBrains server with your local settings and use them as the shared ones.

![The Settings Sync window](https://resources.jetbrains.com/help/img/idea/2025.3/settings_sync_list_first_time.png)

Click Enable Backup and Sync.

  5. In the other IDE instance, where you want these settings to be applied, open Settings `Ctrl+Alt+S`, go to Backup and Sync, and then click Enable Backup and Sync.

  6. In the Backup and Sync dialog that opens, select Get Settings from Account.




Your local settings will be automatically synchronized with the settings stored on the JetBrains server each time you modify a setting and each time the JetBrains server receives setting updates from another IDE.

Plugin states are synchronized as follows:

  * If a plugin is installed on both IDEs, Backup and Sync synchronizes the plugin state (enabled or disabled) between the two IDEs.

  * If a plugin is installed and enabled on one IDE but is not installed on the other IDE, Backup and Sync will install it on the other IDE.

  * If a plugin is installed and disabled on one IDE, and it is not installed on the other IDE, Backup and Sync will not install it on the other IDE.

  * If you uninstall a plugin, and it is installed on the other IDE, Backup and Sync will disable but not uninstall it on the other IDE.




### Disable settings backup and synchronization

You can either disable settings backup and synchronization for a single IDE or completely remove all settings from the JetBrains cloud server and disable synchronization for all IDEs connected to your JetBrains account.

  1. In the upper-right corner of the IntelliJ IDEA window, click the gear icon ![the Gear icon](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.settings.svg) and select Backup and Sync.

  2. On the Backup and Sync page that opens, click Disable Backup and Sync.

  3. Confirm disabling settings synchronization. To disable synchronization on all of your IDEs, select Remove data from JB account and disable for all IDEs.




### Settings synchronized with Backup and Sync

This list describes settings categories that you can [enable and disable](#synced-settings-available) on the Backup and Sync page. The list is not comprehensive, but it gives you an overview of the IDE settings that compose each category.

UI settings
    

  * Appearance & Behavior | Appearance

  * Appearance & Behavior | Menus and Toolbars

  * Appearance & Behavior | Notifications

  * Appearance & Behavior | Quick Lists

  * Editor | Font

  * Editor | Color Scheme



Code settings
    

  * Editor | General

  * Editor | Code Editing

  * Editor | Code Style

  * Editor | File Encodings

  * Editor | Live Templates

  * Editor | File Types

  * Editor | Inlay Hints

  * Editor | Emmet

  * Editor | Intentions



Tools
    

  * Version Control

  * Build, Execution, Deployment | Debugger

  *   * Tools | Space

  * Tools | Database

  * Tools | CSV Formats

  * Tools | Shared Indexes



System settings
    

  * Appearance & Behavior | System Settings

  * Appearance & Behavior | System Settings | Date Formats

  * Appearance & Behavior | System Settings | Server Certificates

  * Registry keys



