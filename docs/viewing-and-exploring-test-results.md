[//]: # (Source: https://www.jetbrains.com/help/idea/viewing-and-exploring-test-results.html)
[//]: # (Downloaded: 2025-12-17 20:06:16)

## Export and import test results

### Export test results to a file

  1. Click ![The More button](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.moreVertical.svg) on the test results toolbar, then click ![](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.export.svg) Export Test Results. 

![Using the test results toolbar to export test results](https://resources.jetbrains.com/help/img/idea/2025.3/ij_export-tests-button.png)
  2. Select the format in which you want to save the file:

     * HTML: generate an HTML file from a pre-defined template.

     * XML: use this format if you want to import this file later to IntelliJ IDEA.

     * Custom, apply XSL template: use your custom [XSL](https://www.w3schools.com/xml/xsl_intro.asp) template to generate an HTML file from the raw XML output. Click ![Browse button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.inline.browse.svg) next to this option and select the *.xsl code style definition file.

  3. Specify the name of the output file and its location.

  4. If you want to open the file in your browser after you export it, select the Open exported file in browser checkbox. Click OK. 

![Exporting test results to a file](https://resources.jetbrains.com/help/img/idea/2025.3/ij_export-test-results.png)



### Import test results

  1. To load a previously exported file, click ![Import Tests from File](https://resources.jetbrains.com/help/img/idea/2025.3/app-client.expui.general.import.svg) on the test results toolbar.

![Importing test results](https://resources.jetbrains.com/help/img/idea/2025.3/ij_import-tests.png)

If you have not run any tests yet, and the tool window with the test results toolbar is not available, press `Ctrl+Shift+A` and type `Import Tests from File`.

  2. In the file system dialog that opens, select the .xml file with test results and click Open.

Import only works for the test results in .xml format.



