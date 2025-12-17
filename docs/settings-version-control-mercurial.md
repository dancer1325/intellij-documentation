[//]: # (Source: https://www.jetbrains.com/help/idea/settings-version-control-mercurial.html)
[//]: # (Downloaded: 2025-12-17 20:02:25)

# Mercurial

Use this page to specify the version control settings to be applied to the directories of your project that are under Mercurial version control.

Item| Description  
---|---  
Path to hg executable| Specify the location of the Mercurial executable file. Enter the path manually, or click the Browse button ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and select the path in the dialog that opens.If you followed the standard installation procedure, the default location is /Applications/TortoiseHg.app/Contents/MacOS/hg or /usr/local/bin for Linux and macOS and /Program Files/TortoiseHG for Windows.It is recommended that you add the path to the Mercurial executable file to the `PATH` [variable](absolute-path-variables.html). In this case, you can specify only the executable name, the full path to the executable location is not required.  
Test| Click this button to verify the path to the Mercurial executable.  
Execute branch operations on all roots| This option only becomes available if you have a multirooted project, that is there are several Mercurial repositories within a single project.Select this option if you want branch operations (such as `checkout`, `merge`, and so on.) to be applied synchronously to all repositories within your project.  
Check for incoming and outgoing changesets| Select this option if you want IntelliJ IDEA to detect incoming and outgoing changes in the background mode. IntelliJ IDEA will automatically request the server for incoming and outgoing changesets every 5 minutes.  
Ignore whitespace differences in annotations| Select this option if you want white spaces to be ignored when annotating, and, thus, get more meaningful annotations and cast out senseless ones.  
  
14 May 2025

[GitHub](settings-version-control-github.html)[Perforce](settings-version-control-perforce.html)
