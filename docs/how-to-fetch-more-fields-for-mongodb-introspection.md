[//]: # (Source: https://www.jetbrains.com/help/idea/how-to-fetch-more-fields-for-mongodb-introspection.html)
[//]: # (Downloaded: 2025-12-17 19:28:52)

# MongoDB introspection

You can observe MongoDB collections and fields in Database tool window.

IntelliJ IDEA fetches the first 10 documents from each collection to get information about the fields. You can customize this behavior by specifying the `fetch_documents_for_metainfo` JDBC parameter on the Advanced tab of the Data Sources and Drivers dialog ( `Shift+Enter`) .

### Fetch more documents

  1. In the Database tool window, right-click MongoDB data source and select Properties.

  2. Click the Advanced tab.

  3. In the parameter table, scroll down till you see `fetch_documents_for_metainfo`.

  4. Double-click the Value cell of the `fetch_documents_for_metainfo` parameter.

  5. Specify the required value.

![Fetch more documents for MongoDB introspection](https://resources.jetbrains.com/help/img/idea/2025.3/db_fetch_documents_for_metainfo.png)



28 October 2025

[Pre-introspected objects from system catalogs](pre-introspected-objects-from-system-catalogs.html)[Database objects](database-objects.html)
