[//]: # (Source: https://www.jetbrains.com/help/idea/settings-tools-python-integrated-tools.html)
[//]: # (Downloaded: 2025-12-17 20:02:04)

# Python Integrated Tools

This page only appears when Python Plugin is [installed and enabled](managing-plugins.html)!

Use this page to configure requirements management file, default test runner, and documentation strings treatment.

Item| Description  
---|---  
Package requirements file| Type the name of the requirements file, or click the browse button, and select the desired requirements file from the file system using the Select Path dialog.  
Default test runner| Select the test run/debug configuration that IntelliJ IDEA will suggest every time you choose Run on the context menu of a test case. The possible options are:

  * Unittests
  * pytest
  * Nosetests
  * Twisted Trial

  
Detect tests in Jupyter Notebooks| Select this checkbox if you want to include Jupyter Notebook files in the scope of unit test detection.  
Docstring format| Select the format of the documentation strings to be recognized by IntelliJ IDEA. Depending on the selected docstring format, IntelliJ IDEA will generate the stub documentation comments and render text in the [show quick documentation](viewing-reference-information.html#inline-quick-documentation):

  * Plain: on pressing `Enter` or Space after opening quotes, an empty stub is generated; quick documentation shows as plain text.
  * reStructuredText: on pressing `Enter` or Space after opening quotes, stub doc comment is generated according to [reStructuredText](http://docutils.sourceforge.net/rst.html) format; the quick documentation is rendered by Docutils.
  * NumPy: on pressing `Enter` or Space after opening quotes, stub doc comment is generated according to the [NumPy](http://sphinxcontrib-napoleon.readthedocs.org/en/latest/example_numpy.html) format; the quick documentation is rendered by [Napoleon](https://sphinxcontrib-napoleon.readthedocs.org/en/latest/) and Docutils.
  * Google: on pressing `Enter` or Space after opening quotes, stub doc comment is generated according to [Google](http://sphinxcontrib-napoleon.readthedocs.org/en/latest/example_google.html) format; the quick documentation is rendered by [Napoleon](https://sphinxcontrib-napoleon.readthedocs.org/en/latest/) and Docutils.

All types of docstrings feature:

  * Proper generation of docstrings
  * Updates after applying intention actions and quick-fixes
  * Coding assistance
  * Autocompletion for section headers

The information provided in the docstrings is used for code insight.  
Analyze Python code in docstrings| If this checkbox is selected, IntelliJ IDEA highlights the code examples and performs syntax checks and code inspections.If this checkbox is not selected, the code fragments inside docstrings are not analyzed.  
Render external documentation for `stdlib`.| Enables showing documentation for standard library functions from <http://docs.python.org> in View | Quick Documentation.  
Sphinx working directory| Specify the path to the folder that contains .rst files and the conf.py configuration. IntelliJ IDEA uses it to recognize custom roles and provide accurate highlighting and rendering for Sphinx documentation.  
Treat .txt files as reStructuredText| If this checkbox is selected, the files with .txt extension will be highlighted same way, as the files with .rst extension.  
  
05 August 2025

[Python External Documentation](settings-tools-python-external-documentation.html)[Python Plots](python-plots.html)
