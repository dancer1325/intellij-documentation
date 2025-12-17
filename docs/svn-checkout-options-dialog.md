[//]: # (Source: https://www.jetbrains.com/help/idea/svn-checkout-options-dialog.html)
[//]: # (Downloaded: 2025-12-17 20:03:41)

# SVN Checkout Options dialog

This dialog appears when you have selected the repository you want to check out and the destination folder.

Item| Description  
---|---  
Checkout| This read-only field shows the selected source repository.  
Destination| From this list, select the directory to create the working copy in. Choose one of the available folders or click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and select the relevant folder in the dialog that opens.  
Update / Switch to revision| In this area, specify the revision to check out. The available options are: 

  * HEAD \- select this option to have the latest revision checked out.
  * Specified \- select this option to have IntelliJ IDEA check out a specific earlier revision. Type the revision number in the field or click Browse ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and select the relevant revision from the Changes Browse that opens.

  
Depth| Use this drop-down list to specify the range of recursion into subdirectories. The available options are: 

  * Empty: select this option to involve only the current file.
  * Files: select this option to involve the files in the folder.
  * Immediates: select this option to involve direct children of the current file.
  * Infinity: select this option to enable full recursion.

  
Include external locations| Select this checkbox to have [externals](http://svnbook.red-bean.com/en/1.5/svn.advanced.externals.html) included in the working copy.  
  
28 June 2024

[Check Out From Subversion dialog](check-out-from-subversion-dialog.html)[Configure Subversion Branches](configure-subversion-branches.html)
