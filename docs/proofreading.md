[//]: # (Source: https://www.jetbrains.com/help/idea/proofreading.html)
[//]: # (Downloaded: 2025-12-17 19:56:20)

## Local and cloud processing modes

IntelliJ IDEA supports two modes:

  * Local processing for grammar, style, and spelling checks is enabled by default. These checks are performed locally on your device and do not require an internet connection.

  * Cloud processing provides advanced checks and assistance features powered by cloud-based models.

For the best performance and accuracy, we recommend enabling cloud processing in the settings. This mode ensures accurate grammar, style, and spelling checks by using the latest machine learning models.




### Connect to Writing Assistance Cloud

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Natural Languages.

  2. Click Enable Cloud next to Language processing.

  3. In the dialog that opens, click Sign In.




After you apply the changes, you can [configure rules per domain](grammar.html#configure_rules) in Settings | Editor | Natural Languages | Grammar and Style on the Rules tab.

When you connect to the cloud, a widget appears in the status bar. Use it to quickly switch between writing styles and access writing style settings.

![Writing style widget in status bar](https://resources.jetbrains.com/help/img/idea/2025.3/writing_style_widget.png)

### Disconnect from the cloud

If you decide to stop using Writing Assistance Cloud and switch to local processing of your data, you can switch IntelliJ IDEA back to the local mode.

  1. Press `Ctrl+Alt+S` to open settings and then select Editor | Natural Languages.

  2. Next to Language processing, click Disable Cloud.



