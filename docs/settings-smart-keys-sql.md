[//]: # (Source: https://www.jetbrains.com/help/idea/settings-smart-keys-sql.html)
[//]: # (Downloaded: 2025-12-17 20:01:43)

# Smart Keys settings: SQL

Use this settings page to configure typing assistance features in SQL.

For more information about SQL support in IntelliJ IDEA, refer to [Database Tools and SQL](relational-databases.html).

Item| Description  
---|---  
Insert string concatenation on Enter| You may want to turn this option off, if the DBMS you are working with supports multiline string literals:Say, there is the following fragment for PostgreSQL `text` value `notes`: SET notes = 'Lightest element'and the caret is in front of the word `element`.If the option is on, and you press `Enter`, the fragment will change to: SET notes = 'Lightest ' || 'element'Otherwise, the fragment will change to: SET notes = 'Lightest element'  
Close code blocks on Enter| When you start a code block with an opening keyword (BEGIN, LOOP, BEGIN TRY, and others) and press `Enter`, the code block closes with the corresponding closing keywords (END, END LOOP, END TRY, and others).![Close code blocks on Enter](https://resources.jetbrains.com/help/img/idea/2025.3/db_close_code_blocks_on_enter.png)  
  
23 June 2025

[Smart Keys settings: Ruby](settings-smart-keys-ruby.html)[Smart Keys settings: Scala](settings-smart-keys-scala.html)
