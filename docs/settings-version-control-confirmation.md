[//]: # (Source: https://www.jetbrains.com/help/idea/settings-version-control-confirmation.html)
[//]: # (Downloaded: 2025-12-17 20:02:20)

## Confirmation

When files are created| In this section, specify whether and how to put a file created in IntelliJ IDEA under version control:

  * Ask: newly created files are put under version control after you specify the options in the dialog that opens.
  * Add silently: newly created files are automatically added to version control without any notification. Apply files created outside IntelliJ IDEA: if you select this option, files created outside IntelliJ IDEA will also be placed under version control silently.
  * Do not add: newly created files remain unversioned, and you can put them under version control later.

  
---|---  
When files are deleted| In this section, specify whether and how to remove a file from version control when the file is deleted:

  * Ask: files removed locally are also removed from VCS after you have selected it in the dialog that opens.
  * Remove silently: all files removed locally are removed from VCS without asking for confirmation.
  * Do not remove: files removed locally remain under version control.

  
Show options before| Select when to show confirmation options.

  * Checkout (relevant for Subversion only).
  * Update: the confirmation dialog will ask if you want to update your project by [merging](apply-changes-from-one-branch-to-another.html#merge) incoming changes into the current branch or [rebasing](apply-changes-from-one-branch-to-another.html#rebase-branch) the current branch on top of incoming changes.

  
Prompt to unlock files set to read-only if you attempt to edit them| This option is relevant for Perforce and Subversion. Select it if you want the system to offer you to unlock read-only files when you open a file in the editor and try to modify it.
