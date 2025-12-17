[//]: # (Source: https://www.jetbrains.com/help/idea/configure-the-sql-code-style.html)
[//]: # (Downloaded: 2025-12-17 19:21:37)

## Apply the original case from the declaration

IntelliJ IDEA can format names of variables, procedures, and functions as you defined them initially. For example, if you defined the `get_Amount` function in the `CREATE PACKAGE` statement, you want the same case throughout your code, not `GET_AMOUNT` or `get_amount`.

To apply this case throughout the file, IntelliJ IDEA must find the declaration of these variables, procedures, and functions (for example, in the `CREATE PACKAGE` statement). To apply the case in multiple files, create [a DDL data source](ddl-data-sources.html) from these files.

### Apply the declaration case for a file

  1. Open settings by pressing `Ctrl+Alt+S` and navigate to Editor | SQL.

  2. Select the dialect in which you want to apply the original case from the declaration.

  3. Click the Case tab and select the Use original case checkbox.

  4. Click OK.

  5. Click Code | Reformat Code or press `Ctrl+Alt+L`.

On the following image, you can see Pack_1.sql and Pack_2.sql with identical code. Pack_1.sql is not reformatted. Pack_2.sql was reformatted with the Use original case checkbox enabled. In Pack_2.sql, the case from the package declaration was applied throughout the whole file.

[![Enable the declaration case for a file](https://resources.jetbrains.com/help/img/idea/2025.3/db_enable_declaration_case_for_file.png)](https://resources.jetbrains.com/help/img/idea/2025.3/db_enable_declaration_case_for_file.png)



### Apply the declaration case in multiple files

  1. Create [a DDL data source](ddl-data-sources.html) from the files for which you want to apply the declaration case.

  2. Open settings by pressing `Ctrl+Alt+S` and navigate to Editor | SQL.

  3. Select the dialect in which you want to apply the declaration case settings.

  4. Click the Case tab and select the Use original case checkbox.

  5. Click OK.

  6. Click Code | Reformat Code or press `Ctrl+Alt+L` to apply the declaration case in any file of the DDL data source.



