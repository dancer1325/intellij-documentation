[//]: # (Source: https://www.jetbrains.com/help/idea/working-with-the-hibernate-console.html)
[//]: # (Downloaded: 2025-12-17 20:07:32)

## Run the Hibernate console with custom JVM options

The Hibernate console is a Java process. If necessary, you can start it with custom JVM options:

  1. Create an Application run configuration

Go to Run | Edit Configurations, click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg), and select Application.

  2. In the VM options field, specify the options that you want to pass to the JVM when it starts. The rest of the run configuration settings don't matter, and you don't need to specify them.

Click OK to save the run configuration.

  3. When you [open the Hibernate console](#open-hibernate-console), IntelliJ IDEA will display an additional VM and Env Configuration popup with the available run configurations. Select the one with the necessary JVM options or run with the default settings.



