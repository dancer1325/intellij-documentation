[//]: # (Source: https://www.jetbrains.com/help/idea/vagrant.html)
[//]: # (Downloaded: 2025-12-17 20:06:00)

# Vagrant

On this page, enable [Vagrant](http://www.vagrantup.com/) support in IntelliJ IDEA, specify the location of the VagrantFile, and handle the list of Vagrant base boxes to use in creation of virtual boxes (instances).

  1. Make sure that [Vagrant](https://www.vagrantup.com/downloads) and [Oracle's VirtualBox](https://www.virtualbox.org/) are downloaded, installed, and configured on your computer as described in [Vagrant](vagrant-support.html).

  2. Make sure that the parent folders of the following executable files are added to the system PATH variable: 

     * vagrant.bat or vagrant from your Vagrant installation. This should be done automatically by the Vagrant installer.

     * VBoxManage.exe or VBoxManage from your Oracle's VirtualBox installation.




Before you start working with Vagrant, make sure that:

  1. [Vagrant](http://www.vagrantup.com/) is downloaded and installed.

  2. Install and enable the Vagrant [plugin](managing-plugins.html).

The plugin is _not_ bundled with IntelliJ IDEA, but it can be [installed](managing-plugins.html) from JetBrains Marketplace. 




Item| Description  
---|---  
Vagrant executable| Specify the fully qualified address of the executable file: vagrant.bat for Windows, vagrant for Unix and macOS. Type the path manually, or click the browse button and locate the desired file in the dialog that opens.  
Instance folder| Specify here the fully qualified path to the directory, where the task `vagrant init` has been executed, and the Vagrantfile is initialized and stored.A Vagrantfile is a configuration file that defines the instance (virtual machine) you need. The file contains the virtual IP address, port mappings, and the memory size to assign. The file can specify which folders are shared and which third-party software should be installed. According to the Vagrantfile your instance (virtual machine) is configured, provisioned against the relevant Vagrant base box, and deployed on your computer. A Vagrantfile is created through the `vagrant init` command.When creation of an instance (virtual machine) is invoked either through the `vagrant up` command or through the Tools | Vagrant | Up menu option, IntelliJ IDEA looks for the Vagrantfile in the directory specified in the Instance folder field. For more information, refer to <http://docs.vagrantup.com/v2/vagrantfile/>.You can create a Vagrantfile in any directory and appoint it as instance folder. If the field is empty, IntelliJ IDEA will treat the project root as the instance folder and look for a Vagrantfile in it.  
Provider| Use this field to specify the [provider](http://docs.vagrantup.com/v2/providers/configuration.html) to be used by `vagrant up` command. If this field is left blank, the default provider is used.  
Environment variable| Click the ellipsis button or press `Shift+Enter` to specify the shell variables to be used to configure the providers' behavior.  
Boxes and Plugins tabs  
Boxes| This list shows the predefined [Vagrant base boxes](http://docs.vagrantup.com/v2/boxes.html) available in IntelliJ IDEA.Each item presents a Vagrant base box on which Vagrant configures and launches its instances (virtual machines). The entries of this list correspond to the output of the command `vagrant box list`. |   
---  
![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)| `Alt+Insert`| Click this button to download a new base box. This command corresponds to `vagrant box add <name> <URL>`. By default, IntelliJ IDEA suggests the URL to the lucid32 box   
![Remove a box](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)| `Alt+Delete`| Click this button to remove the selected Vagrant base box. The box and the nested files are physically deleted from the disk. This command corresponds to `vagrant box remove <name>`  
  
Plugins| Use this table to view and change the list of available plugins.|   
---  
![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)| `Alt+Insert`| Click this button to install a new Vagrant plugin.  
![Remove the selected plugin](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)| `Alt+Delete`| Click this button to remove the selected plugin.  
![Update the plugin](https://resources.jetbrains.com/help/img/idea/2025.3/app.javaee.updateRunningApplication.svg)| | Click this button to update the selected plugin.  
![Attach a license to the plugin](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.annotate.svg)| | Use this button to attach a license to the selected plugin.  
  
05 November 2025

[Startup Tasks](settings-tools-startup-tasks.html)[XPath Viewer](xpath-viewer.html)
