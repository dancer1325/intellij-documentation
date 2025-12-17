[//]: # (Source: https://www.jetbrains.com/help/idea/run-debug-multiple.html)
[//]: # (Downloaded: 2025-12-17 19:59:05)

## Parallel launch with a compound run/debug configuration

A Compound run configuration lets you launch several run/debug configurations simultaneously.

The exact order of launching configurations within a compound configuration is not guaranteed.

### Create a compound run/debug configuration

  1. [Create a run/debug configuration](run-debug-configuration.html#createExplicitly) for each app and process that should be launched in your session.

  2. Go to Run | Edit Configurations. Alternatively, press `Alt+Shift+F10`, then `0`. 

  3. In the Run/Debug Configurations dialog, click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) or press `Alt+Insert`, then select Compound. 

  4. Specify the run/debug configuration name in the Name field. This name will be used to identify the run/debug configuration in lists and menus. 

  5. To include a new run/debug configuration into the compound configuration , click Add ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select the desired one from the list.

  6. Apply the changes and close the dialog. 



