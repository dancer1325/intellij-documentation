[//]: # (Source: https://www.jetbrains.com/help/idea/full-text-search-for-databases.html)
[//]: # (Downloaded: 2025-12-17 19:27:19)

## Full-text search options

Option| Description  
---|---  
Match case| Searches only for those instances that are written the same way as the query (preserving the case). A search for `Index` will return `Index`, `Indexes`, `Indexing` but not `index`.  
Contains| Searches for a given combination of characters in words. For example, if you search for `ETTE`, you receive all `LIKE '%ETTE%'` results (`ANNETTE`, `JEANETTE`, `GILLETTE`, `BETTE`) from all the columns.![Search anywhere in string](https://resources.jetbrains.com/help/img/idea/2025.3/db_full_text_search_anywhere.png)  
Starts with| Searches for a given combination of characters in the word beginning. For example, if you search for `JO`, you receive all `LIKE 'JO%'` results (`JOHNSON`, `JONES`, `JOYCE`, `JOAN`) from all the columns.![Prefix search](https://resources.jetbrains.com/help/img/idea/2025.3/db_full_text_search_prefix.png)  
Ends with| Searches for a given combination of characters in the word beginning. For example, if you search for `TIN`, you receive all `LIKE '%TIN'` results (`MARTIN`, `AUSTIN`, `KRISTIN`, `JUSTIN`) from all the columns.![Suffix search](https://resources.jetbrains.com/help/img/idea/2025.3/db_full_text_search_suffix.png)  
Matches| Searches for an exact combination of characters. For example, if you search for `DAVIS`, you receive all `LIKE 'DAVIS'` results `DAVIS` from all the columns.![Full match search](https://resources.jetbrains.com/help/img/idea/2025.3/db_full_text_search_full_match.png)  
LIKE pattern| Searches for a combination of characters and [SQL wildcards](https://www.w3schools.com/sql/sql_wildcards.asp). For example, you can search for `a_%_%` and find any `LIKE 'a_%_%'` results that start with `a` and have at least three characters in length `ANDERSON`, `ALLEN`, `AMY`, `ANNA`.![LIKE pattern search](https://resources.jetbrains.com/help/img/idea/2025.3/db_full_text_search_like_pattern.png)  
Text columns| Searches only in columns that support the LIKE operation. For example, CHAR, VARCHAR, TINYTEXT, TEXT, and DATE (Oracle).  
Only columns with full-text search indexes| Searches only in columns that have a created index. This feature is supported only for PostgreSQL, MySQL, and MariaDB. The query for PostgreSQL is `where col @@ plainto_tsquery('query')`. The query for MySQL and MariaDB is `where match(col) against ('query' in natural language mode)`.  
Numeric columns| Searches only in columns with the numeric data type like INT, MEDIUMINT, SMALLINT, BIGINT, and others.  
All columns| Searches in all types of columns. For example, you can run this search to find a JSON element.  
Show first N matches per table/view| Limits the number of found results for a table or a view.
