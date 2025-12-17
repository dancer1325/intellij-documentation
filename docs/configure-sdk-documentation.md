[//]: # (Source: https://www.jetbrains.com/help/idea/configure-sdk-documentation.html)
[//]: # (Downloaded: 2025-12-17 19:21:35)

# Configure SDK documentation

You can add documentation to IntelliJ IDEA so that you can get information about symbols and method signatures right from the editor in the [Quick Documentation](viewing-reference-information.html#inline-quick-documentation) popup.

You can also configure external documentation by specifying the path to the reference information online. External documentation opens the necessary information in a browser so that you can navigate to related symbols and keep the information for further reference at the same time.

In SDKs, documentation is normally bundled. However, you can configure it manually in case you need additional or specific documentation or if you work offline.

### Specify SDK documentation paths

To view external SDK documentation, configure the documentation URL first.

  1. In the Project Structure dialog `Ctrl+Alt+Shift+S`, select SDKs.

  2. Select the necessary SDK version if you have several SDKs configured and open the Documentation Path tab on the right.

  3. Click the ![Specify URL](https://resources.jetbrains.com/help/img/idea/2025.3/app.toolbarDecorator.addLink.svg) icon, enter the external documentation URL, and click OK.

For example, for Java 20, type `https://docs.oracle.com/en/java/javase/25/docs/api/`.

![Specifying SDK documentation paths](https://resources.jetbrains.com/help/img/idea/2025.3/add-sdk-docs.png)
  4. Apply the changes and close the dialog.




### Access SDK documentation offline

If you work offline, you can view external documentation locally.

  1. Download the documentation package of the necessary version.

The documentation package is normally distributed in a ZIP archive that you need to unpack once it is downloaded.

For example, you can download the official [Java SE Development Kit 25 Documentation](https://www.oracle.com/java/technologies/javase-jdk25-doc-downloads.html) and unzip it.

  2. In the Project Structure dialog `Ctrl+Alt+Shift+S`, select SDKs.

  3. Select the necessary JDK version if you have several JDKs configured and open the Documentation Path tab on the right.

  4. Click the ![Add](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) icon and specify the directory with the downloaded documentation package (for example, C:\Users\jetbrains\Desktop\docs\api).

  5. Apply the changes and close the dialog. 




When the documentation is configured, you can [open it in the editor](viewing-reference-information.html#inline-quick-documentation).

11 November 2025

[Supported Java versions and features](supported-java-versions.html)[Libraries](library.html)
