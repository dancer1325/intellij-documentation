[//]: # (Source: https://www.jetbrains.com/help/idea/sql-for-mongodb.html)
[//]: # (Downloaded: 2025-12-17 20:03:13)

## Data types

IntelliJ IDEA supports the following data types:

  * String, Integer, Float, Boolean

  * NULL, NAN, INFINITY

  * Arrays (`[1, 2, 3]`) and maps (`{a: 1, b: 2, c: 3}`)




Arrays and maps may include any expressions.

SELECT [1, 3 + 1 - 2, price] AS elements FROM sales; SELECT {a: 1 + 2, b: NULL, c: FALSE, d: [1, 2]} FROM sales;

You can use string literals in single or double quotation marks.

Write column names without quotation marks or use a grave accent (```).

SELECT _id, `acquisitions`, `category_code`, `description`, email_address, phone_number FROM companies WHERE category_code = 'social' AND description = "Mobile Dating";
