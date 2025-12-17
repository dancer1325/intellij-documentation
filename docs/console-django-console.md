[//]: # (Source: https://www.jetbrains.com/help/idea/console-django-console.html)
[//]: # (Downloaded: 2025-12-17 19:22:22)

# Console. Django Console and manage.py options

This page only appears when Python Plugin is [installed and enabled](managing-plugins.html)!

This page only appears when Django support is enabled!  
---  
  
Use this page to define the Python interpreter, its options, starting script, and so on for the Django console.

Item| Description  
---|---  
Environment variables| This field shows the list of environment variables. If the list contains several variables, they are delimited with semicolons.To fill in the list, click the browse button, or press `Shift+Enter` and specify the desired set of environment variables in the Environment Variables dialog.To create a new variable, click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg), and type the desired name and value.You might want to populate the list with the variables stored as a series of records in a text file, for example:  Variable1 = Value1 Variable2 = Value2  Just copy the list of variables from the text file and click Paste (![Paste](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.paste.svg)) in the Environmental Variables dialog. The variables will be added to the table. Click Ok to complete the task. At any time, you can select all variables in the Environment Variables dialog, click Copy ![Copy](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.copy.svg), and paste them into a text file.   
Python Interpreter| From the list, select one of the pre-configured Python interpreters.  
Interpreter options| In this field, specify the string to be passed to the interpreter. If necessary, click Enter, and type the string in the editor.  
Working directory| Specify a directory to be used by the running console. When this field is left blank, the project directory will be used.  
Configure interpreters| If the desired interpreter is missing in the list, click this link to open the _Python interpreters_ page, and configure an interpreter or virtual environment.  
Add content roots to PYTHONPATH| Select this checkbox to have the content roots added to the PYTHONPATH.  
Add source roots to PYTHONPATH| Select this checkbox to have the source roots added to the PYTHONPATH.  
Starting script| In this editor area, type the script to be executed in the console after its start-up and initialization. Note that syntax highlighting, code completion, import assistance, documentation, inspections and quick fixes are available in this editor:![Starting script](https://resources.jetbrains.com/help/img/idea/2025.3/py_startingScript.png)By default, this area contains the following script, which causes printing out a header information and extending the system paths: import sys; print('Python %s on %s' % (sys.version, sys.platform)) sys.path.extend([WORKING_DIR_AND_PYTHON_PATHS]) The `WORKING_DIR_AND_PYTHON_PATHS` variable is hardcoded in IntelliJ IDEA. It displays two paths: the project root and the working directory. The project root is the top-level directory of your project. The working directory may coincidence with the project root if not explicitly defined in the Working directory field.If you want to omit such a printout, delete this script.  
  
20 October 2025

[Console. Python Console](console-python-console.html)[Deployment](settings-deployment.html)
