[//]: # (Source: https://www.jetbrains.com/help/idea/settings-tools-python-external-documentation.html)
[//]: # (Downloaded: 2025-12-17 20:02:02)

## Python External Documentation

To view Python external documentation, you need to configure the documentation URL first. IntelliJ IDEA comes with the URLs for pandas, wx, kivy, PySide, PyQt5, PyQt4, matplotlib, pyramid, flask, and gtk. You can modify the predefined set of URLs or add a new one in the project Settings.

![Configuring external documentation](https://resources.jetbrains.com/help/img/idea/2025.3/python_external_doc_settings.png)

Item| Description  
---|---  
Module Names| This column shows the names of the modules, whose documentation you want to have visible in browser on invoking View | External Documentation, or pressing `Shift+F1`, for example, pandas.  
URL Pattern| This column shows existing patterns of the URLs to the external documentation, or its local address, for example, https://pandas.pydata.org/pandas-docs/stable/generated/{element.qname}.htmlIf external documentation resides locally, specify the local path to it .  
![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)| Click this button to add to the list a new module and its URL pattern or local address.  
![the Edit button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.edit.svg)| Click this button to change the name or URL pattern of the selected module.Double-clicking an entry in the table produces the same result.  
![the Remove button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.remove.svg)| Delete the selected module from the list.
