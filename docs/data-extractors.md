[//]: # (Source: https://www.jetbrains.com/help/idea/data-extractors.html)
[//]: # (Downloaded: 2025-12-17 19:23:57)

## Supported file formats

The list of available scripts and supported file formats is as follows:

  * Predefined scripts. Use them to export data as a set of `INSERT` or `UPDATE` statements, [TSV and CSV](https://en.wikipedia.org/wiki/Delimiter-separated_values) files, [Excel XLSX](https://en.wikipedia.org/wiki/Microsoft_Excel) files, [Markdown](https://en.wikipedia.org/wiki/Markdown), HTML tables, and [JSON](https://en.wikipedia.org/wiki/JSON) format.

    1. Built-in

Script| File format  
---|---  
SQL Inserts| .sql  
SQL Updates  
Where Clause  
  
    2. CSV

Script| File format  
---|---  
CSV| .csv  
TSV| .tsv  
Pipe-separated| .txt  
  
Use the [CSV format configurations](#creating-a-dsv-based-extractor) to create your own format that is based on CSV or any DSV format.

    3. Scripted

Script| File format  
---|---  
CSV| .csv  
TSV| .tsv  
Excel| .xlsx, .xls  
HTML (groovy)| .html  
HTML (js)  
JSON| .json  
Markdown| .md  
One-row| .sql  
SQL-Insert-Multirow  
SQL-Insert-Statements  
Pretty| .txt  
XML| .xml  
  
  * [Custom data extractors.](#add-a-custom-extractor) Create them using Groovy or JavaScript and the provided API.



