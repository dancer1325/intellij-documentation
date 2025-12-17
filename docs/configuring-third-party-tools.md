[//]: # (Source: https://www.jetbrains.com/help/idea/configuring-third-party-tools.html)
[//]: # (Downloaded: 2025-12-17 19:22:09)

## Web browsers

You can use a web browser to open any file from your project. By default, it is used to preview the output of an HTML file or run and debug web applications.

### Open a file in a web browser

To open a file that is intended to be rendered by a web browser (HTML, XML, JSP, and so on), do one of the following:

  * Open the file in the editor and press `Alt+F2`.

  * Right-click the file in the [Project tool window](project-tool-window.html) and select Open in Browser.

  * In the main menu, go to View | Open in Browser.

  * Use the browser popup in the top right part of the editor window (appears on hover). Click the browser button to open the web server file URL, or `Shift+Click` it to open the local file URL.

![The Browser popup in the editor](https://resources.jetbrains.com/help/img/idea/2025.3/editor-browser-popup.png)



The Open in Browser action is not available for other file types. However, you can still execute it using Find Action `Ctrl+Shift+A`.

### View and configure the list of browsers

By default, IntelliJ IDEA supports some of the most popular browsers, which are configured automatically, if available.

  * In the Settings dialog (`Ctrl+Alt+S`) , select Tools | Web Browsers and Preview.


![The Web Browsers page in Settings](https://resources.jetbrains.com/help/img/idea/2025.3/settings-tools-web-browsers.png)

If a browser was installed using a standard procedure, the alias in the Path field should point to the right location. If it does not, specify the path to the corresponding executable file.

To add a custom browser, click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and specify the browser name, family, and location of the executable file or macOS application.

### Use custom profile and settings

You can configure custom profiles for Firefox and Chrome family browsers.

  1. In the Settings dialog (`Ctrl+Alt+S`) , select Tools | Web Browsers and Preview.

  2. Select the browser in the list and click ![the Edit button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.edit.svg).

     * For Firefox, specify the path to the profiles.ini file and choose the profile to use. For more information, refer to [Firefox browser profile](http://support.mozilla.com/en-US/kb/Profiles).

     * For Chrome, select Use custom user data directory and specify the location of the [user data directory](https://chromium.googlesource.com/chromium/src/+/master/docs/user_data_dir.md).

You can also specify additional command-line options to use when running Chrome from IntelliJ IDEA. For more information, open `chrome://flags` in the Chrome address bar.



