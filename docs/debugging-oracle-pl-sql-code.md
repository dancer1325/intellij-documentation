[//]: # (Source: https://www.jetbrains.com/help/idea/debugging-oracle-pl-sql-code.html)
[//]: # (Downloaded: 2025-12-17 19:24:24)

## Step 1. Create a PL/SQL object

  1. Right-click the Oracle data source and select New | Query Console.

Alternatively, select one of the existing query files from Query Consoles list (`Ctrl+Shift+F10`).

  2. Type or paste your code in the query file.

  3. Click the Execute button ![the Execute button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.execute.svg) or press `Ctrl+Enter` to run the procedure code.

As a result, you see a created object in the Database tool window (View | Tool Windows | Database).


![Create a PL/SQL object](https://resources.jetbrains.com/help/img/idea/2025.3/pl_sql_debugging_create_procedure.png)

A code snippet of the procedure:

CREATE PROCEDURE simpleprocedure (inval NUMBER) IS tmpvar NUMBER; tmpvar2 NUMBER; total NUMBER; BEGIN tmpvar := 0; tmpvar2 := 0; total := 0; FOR lcv IN 1 .. inval LOOP total := 2 * total + 1 - tmpvar2; tmpvar2 := tmpvar; tmpvar := total; END LOOP; DBMS_OUTPUT.put_line ('TOTAL IS: ' || total); END simpleprocedure; / 
