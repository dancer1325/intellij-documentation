[//]: # (Source: https://www.jetbrains.com/help/idea/run-debug-configurations-dialog.html)
[//]: # (Downloaded: 2025-12-17 19:59:02)

## Common settings

When you edit a run configuration (but not a run configuration template), you can specify the following options:

Item| Description  
---|---  
Name| Specify a name for the run configuration to quickly identify it among others when editing or running.  
Allow multiple instances| Allow running multiple instances of this run configuration in parallel.By default, it is disabled, and when you start this configuration while another instance is still running, IntelliJ IDEA suggests stopping the running instance and starting another one. This is helpful when a run configuration consumes a lot of resources and there is no good reason to run multiple instances.  
Store as project file| Save the file with the run configuration settings to share it with other team members. The default location is .idea/runConfigurations. However, if you do not want to share the .idea directory, you can save the configuration to any other directory within the project.By default, it is disabled, and IntelliJ IDEA stores run configuration settings in .idea/workspace.xml.
