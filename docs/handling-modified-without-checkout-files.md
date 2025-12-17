[//]: # (Source: https://www.jetbrains.com/help/idea/handling-modified-without-checkout-files.html)
[//]: # (Downloaded: 2025-12-17 19:28:38)

# Handle modified without checkout files

If you are going to modify or delete a file under Perforce version control, the read-only status of such file should be removed. IntelliJ IDEA takes care of automatically making files writable. However, you can change read-only status manually, which may happen in a number of ways; for example:

  * With the Clear Read-Only Status option enabled, you make a file writable using a file system.

  * When a read-only file is opened in the editor, you double-click lock icon ![uiStatusLock.png](https://resources.jetbrains.com/help/img/idea/2025.3/uiStatusLock.png) in the status bar.

  * You remove read-only attribute externally, using file properties.




In these cases, the file gets status Modified without checkout and appears in the Commit window.

### To resolve 'modified without checkout' files

  1. In the Commit window, expand Modified without Checkout node, and select the desired file.

  2. From the context menu of the file, choose Check Out. The file becomes writable, and moves to the active changelist.




14 May 2025

[Configure Perforce integration](enabling-and-configuring-perforce-integration.html)[Integrate Perforce files](integrating-perforce-files.html)
