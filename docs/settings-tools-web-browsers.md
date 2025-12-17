[//]: # (Source: https://www.jetbrains.com/help/idea/settings-tools-web-browsers.html)
[//]: # (Downloaded: 2025-12-17 20:02:15)

## Browsers

In this section, specify which browsers will be available for previewing HTML or JSP output. The section shows the browsers from the predefined list and the previously configured custom browser installations, if any. 

IntelliJ IDEA is shipped with a predefined list of most popular browsers that you may install and launch automatically from the IDE during running, debugging, or [previewing the output of an HTML file](editing-html-files.html#ws_html_preview_output). IntelliJ IDEA presumes that you install browsers according to a standard procedure and assigns each installation an alias which stands for the default path to the browser's executable file or macOS application. 

If in your actual browser installation the path to the executable file is different, you need to specify it explicitly in the Path field.

In addition to the predefined browsers, you can configure as many custom browser installations as you need using the controls on the toolbar.

Item| Description  
---|---  
Active| Select this checkbox to enable the use of the respective browser from IntelliJ IDEA. The browser will be added to the context menu of the Open in Browser menu item and its icon will be displayed in the browser icons popup. If this checkbox is cleared, the corresponding browser icon will not appear in the icons toolbar or popup.  
Name| In this column, specify the browser name.  
Family| In this column, specify the family to which the browser belongs.  
Path| In this column, specify the path to the executable. If the browser was installed according to a standard installation procedure, most likely the alias in the Path field points at the right location. If it does not, click ![the Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.ellipsis.svg) and select the actual path in the dialog that opens. In the dialog that opens, select the path to the executable file of the corresponding browser.  
  
### Toolbar

Item| Description  
---|---  
![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)| Click this button to add a custom browser to the list.  
![the Remove button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)| Click this button to delete the selected customer browser from the list. Note that you cannot delete the browsers from the predefined list.  
![the Edit button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.edit.svg)| Click this button to specify a custom profile for Firefox or a browser of the Chrome family. The button is available only when Firefox and Chrome are selected.In the Firefox Settings dialog, specify the [Firefox browser profile](http://support.mozilla.com/en-US/kb/Profiles) to use for previewing output:

  * Path to "profiles.ini": in this field, specify the location of the profiles.ini file, which determines the Firefox profile to be used.
  * Profile: from this list, select the desired predefined profile to use. Learn more at [Firefox browser profile](http://support.mozilla.com/en-US/kb/Profiles).

In the Chrome Settings dialog:

  * Command line options: In this field, enter the command-line options to launch an instance of Chrome. If you need more space, click ![the Expand icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.general.expandComponent.svg), or press `Shift+Enter` to open the editor box. Learn more about Chrome command-line options by opening `chrome://flags` in Chrome. 
  * Use custom user data directory: Select this checkbox to define a user-specific Chrome profile settings to use and specify the location of the [user data directory](https://chromium.googlesource.com/chromium/src/+/master/docs/user_data_dir.md) in the IntelliJ IDEA settings. 

  
![The Previous Occurrence button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.up.svg)![The Next Occurrence button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.down.svg)| Use these buttons to move the selected browser up or down in the list. The order of browsers is important for rendering external resources and previewing files with Web contents.  
![The Copy button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.copy.svg)| Click this button to create a copy of the selected browser.
