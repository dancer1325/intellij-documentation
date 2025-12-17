[//]: # (Source: https://www.jetbrains.com/help/idea/using-multiple-perforce-depots-with-p4config.html)
[//]: # (Downloaded: 2025-12-17 20:05:34)

# Use multiple Perforce depots with P4CONFIG

If your project contains directories that are stored in the different Perforce depots, you might need to switch between them. IntelliJ IDEA uses `P4CONFIG` to automatically switch to the respective depot as you use a Perforce-versioned directory.

`P4CONFIG` is an environment variable that contains the name of the P4CONFIG file without the path. If a certain directory is associated with Perforce (refer to [Version control integration support](enabling-version-control.html)), IntelliJ IDEA seeks for the P4CONFIG file in this directory and its parents; if the file is not found, IntelliJ IDEA looks for it in the bin directory of IntelliJ IDEA installation. When a P4CONFIG file is found, IntelliJ IDEA uses the settings contained in it to connect to the respective Perforce depot.

A sample P4CONFG file might consist of the following lines:

P4CLIENT=MyClient P4USER=MySelf P4PORT=ida:3456 

  1. Create a P4CONFIG file in each directory associated with Perforce.

  2. Create the `P4CONFIG` environment variable that contains the file name without the path.




14 May 2025

[Show Revision Graph and Time-Lapse View](showing-revision-graph-and-time-lapse-view.html)[Work with Perforce offline](perforce-working-offline.html)
