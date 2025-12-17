[//]: # (Source: https://www.jetbrains.com/help/idea/command-line-merge-tool.html)
[//]: # (Downloaded: 2025-12-17 19:21:07)

# Merge files from the command line

Open the Merge dialog to perform a three-way or a two-way merge from the command line.

You can find the executable for running IntelliJ IDEA in the installation directory under bin. To use this executable as the command-line launcher, add it to your system `PATH` as described in [Command-line interface](working-with-the-ide-features-from-command-line.html).

Syntax
    

idea64.exe merge <path1> <path2> [<base>] <output>

Example
    

To perform a three-way merge, you need to specify paths for two modified versions of a file, the base revision (a common origin of both modified versions), and the output file to save merge results:

idea64.exe merge C:\MyProjectCopy\Readme.md C:\FriendsProjectCopy\Readme.md C:\Archive\Readme.md C:\MainProject\Readme.md 

Don't specify the optional base revision if you want to treat the current contents of the output file as the common origin. In this case, if the output is an empty file, this essentially becomes a two-way merge.

By default, IntelliJ IDEA does not provide a command-line launcher. For more information about creating a launcher script for IntelliJ IDEA, refer to [Command-line interface](working-with-the-ide-features-from-command-line.html).

Syntax
    

idea merge <path1> <path2> [<base>] <output>

Example
    

To perform a three-way merge, you need to specify paths for two modified versions of a file, the base revision (a common origin of both modified versions), and the output file to save merge results:

idea merge ~/MyProjectCopy/Readme.md ~/FriendsProjectCopy/Readme.md ~/Archive/Readme.md ~/MainProject/Readme.md 

Don't specify the optional base revision if you want to treat the current contents of the output file as the common origin. In this case, if the output is an empty file, this essentially becomes a two-way merge.

You can find the script for running IntelliJ IDEA in the installation directory under bin. To use this script as the command-line launcher, add it to your system `PATH` as described in [Command-line interface](working-with-the-ide-features-from-command-line.html).

Syntax
    

idea.sh merge <path1> <path2> [<base>] <output>

Example
    

To perform a three-way merge, you need to specify paths for two modified versions of a file, the base revision (a common origin of both modified versions), and the output file to save merge results:

idea.sh merge ~/MyProjectCopy/Readme.md ~/FriendsProjectCopy/Readme.md ~/Archive/Readme.md ~/MainProject/Readme.md 

Don't specify the optional base revision if you want to treat the current contents of the output file as the common origin. In this case, if the output is an empty file, this essentially becomes a two-way merge.

08 October 2024

[Compare files from the command line](command-line-differences-viewer.html)[Tutorial: Use IntellJ IDEA as default command-line merge tool](tutorial-use-idea-as-default-command-line-merge-tool.html)
