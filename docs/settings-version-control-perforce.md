[//]: # (Source: https://www.jetbrains.com/help/idea/settings-version-control-perforce.html)
[//]: # (Downloaded: 2025-12-17 20:02:26)

# Perforce

Use this page to specify the version control settings to be applied to those directories of your project that are under Perforce control

Item| Description  
---|---  
Perforce is online| Select this checkbox to work with Perforce in the online mode.  
Switch to offline mode automatically if Perforce is unavailable| Select this checkbox to have IntelliJ IDEA automatically [go offline](perforce-working-offline.html) as soon as Perforce becomes unavailable and display the corresponding message.  
Use P4CONFIG or default connection| If this option is selected, `P4CONFIG` or the default Perforce connection is used to connect to the Perforce server. Using `P4CONFIG` makes it trivial to switch between Perforce settings for different projects, when necessary.  
Use connection parameters| If this option is selected, the connection credentials (port, client, user name, and charset) are specified manually.  
Port| In this field, type the server and the port which your Perforce client will listen to. For the default Perforce server configuration, it looks like _perforce:1666_.  
Client| In this field, type the name of your Perforce workspace name.  
User| In this field, type your user name to authenticate to the server.  
Charset| From this drop-down list, select the character set to be used.  
Dump Perforce commands to <path>| Select this checkbox to have IntelliJ IDEA create a file P4.output and store the output of Perforce commands in it.  
Use login authentication| When this checkbox is selected, Perforce requires a login to authenticate a user.  
Test Connection| Click this button to check whether the specified settings ensure establishing connection to the Perforce server.  
Path to P4 executable| In this field, specify the path to the Perforce Command Line Client's executable file P4. Click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) to open the Select Path - P4 Configuration dialog and select the executable file in the directories tree.  
Path to P4V executable| In this field, specify the path to the Perforce Visual Client's executable file P4V. Click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) to open the Select Path - P4 Configuration dialog and select the executable file in the directories tree.  
Show branching history ...| Select this checkbox to enable displaying the branch history of a specified file, including all file branch points, edits, and merges.  
Show integrated changelists in committed changes| Select this checkbox to have IntelliJ IDEA point at committed changes that are also integrated to other changelists and provide information on the target changelists that received the content in question.  
Server timeout| In this field, specify the time period in seconds after when the Perforce client cancels its attempts to establish connection to the server.  
Enable Perforce Jobs Support| When this checkbox is selected, user interface for attaching and detaching Perforce jobs to change lists is provided in the Version Control tool window `Alt+9` and in the Commit Changes dialog.  
Find ignored files using P4 executable|   
Always sync local changelists with Perforce| This setting automatically synchronizes changelists between IntelliJ IDEA and Perforce. When enabled, [creating a new changelist](managing-changelists.html) also creates a corresponding Perforce changelist, and any local changelists without a Perforce match are deleted. Disable this setting for manual synchronization control.  
  
08 October 2025

[Mercurial](settings-version-control-mercurial.html)[Subversion](settings-version-control-subversion.html)
