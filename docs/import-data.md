[//]: # (Source: https://www.jetbrains.com/help/idea/import-data.html)
[//]: # (Downloaded: 2025-12-17 19:29:16)

## Restore a full data dump for MySQL and PostgreSQL

You can restore data dumps by using the `mysql` client utility for MySQL, or [pg_restore](https://www.postgresql.org/docs/current/app-pgrestore.html) or [psql](https://www.postgresql.org/docs/current/backup-dump.html) for PostgreSQL. The pg_restore option is used for custom-format `pg_dump -Fc` or directory-format `pg_dump -Fd` dumps. The psql option is used for SQL-format dumps.

If you see no restore options in the context menu, verify that you use a correct JDBC URL for the data source.

### Restore data with mysql or pg_restore

  1. In the Database tool window, right-click a schema or a database and navigate to the Import/Export group:

     * Restore with 'mysql': for MySQL data sources. In the Path to executable field, specify the path to the mysql executable (for example, C:\Soft\mysql-8.0.19-winx64\bin\mysql.exe).

     * Restore with 'pg_restore': for PostgreSQL data sources. The pg_restore option is available for the most database objects except for the data source level.

     * Restore with 'psql': for PostgreSQL data sources. The psql option is available for data sources.

     * Restore with 'pg_restore'/'psql': for PostgreSQL data sources. Includes two tabs: pg_restore and psql. The option is available for databases.

  2. In the Restore with <dump_tool> dialog, specify the path to the restore tool executable in the Path to executable field.

Specify the full explicit path to the dump tool executable.

(Optional) Edit the command-line options in the lower part of the dialog.

  3. Click Run.


![Restore a full data dump with pg_restore](https://resources.jetbrains.com/help/img/idea/2025.3/db_restore_full_dump_with_pg_restore.png)

For PostgreSQL, you can use Restore with "pg_restore" on a table level.

### 'Restore with' dialogs reference

![the Restore with mysql dialog](https://resources.jetbrains.com/help/img/idea/2025.3/db_restore_with_mysql.png)

Item| Description  
---|---  
Where to run| Sets where to run the tool. You can either run it locally or in a Docker container.

  1. Locally
     * Path to executable: Defines the path to the mysql executable on your machine.
  2. In a Docker container This functionality relies on the [Docker](https://plugins.jetbrains.com/plugin/7724-docker) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. For more information, refer to [Open plugin settings](managing-plugins.html#open-plugin-settings). 
     * Server: Sets the server used to run the container.
     * Container: Sets the container to run the mysql executable in.
     * Path to executable: Defines the path to the mysql executable inside the container.If you use the IDE [Docker](https://plugins.jetbrains.com/plugin/7724-docker) plugin, type path to the mysql executable inside the container (for example, `/usr/bin/mysqldump`). 
     * Path to dump (in container): Defines the path to the dump file inside the container.

  
Options  
Database| `--database`Name of the database to connect to.  
Path to dump| Defines the path to the dump file on your machine.  
  
![the Restore with pg_restore dialog](https://resources.jetbrains.com/help/img/idea/2025.3/db_restore_with_pg_restore.png)

Hover over the export option to see the command line arguments in a tooltip.

Item| Description  
---|---  
Where to run| Sets where to run the tool. You can either run it locally or in a Docker container.

  1. Locally
     * Path to executable: Defines the path to the pg_restore executable on your machine.
  2. In a Docker container This functionality relies on the [Docker](https://plugins.jetbrains.com/plugin/7724-docker) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. For more information, refer to [Open plugin settings](managing-plugins.html#open-plugin-settings). 
     * Server: Sets the server used to run the container.
     * Container: Sets the container to run the pg_restore executable in.
     * Path to executable: Defines the path to the pg_restore executable inside the container.If you use the IDE [Docker](https://plugins.jetbrains.com/plugin/7724-docker) plugin, type path to the pg_restore executable inside the container (for example, `/usr/bin/mysqldump`). 
     * Path to dump (in container): Defines the path to the dump file inside the container.

  
Options  
Database| `--dbname`Connect to the specified database and restore directly into it.  
Schemas| `--schema`Restore only objects that are in the specified schema.  
Tables to dump| `--table`Restore only the specified tables.  
Format| `--format`Format of the output:

  * Auto: pg_restore determines the format automatically.
  * Directory: `--format=d`. Directory-format archive. 
  * Custom-format archive: `--format=c`. The pg_dump custom-format archive. 
  * Tar archive: `--format=t`. Tar-format archive. 

  
Path to dump| Defines the path to the dump file on your machine.  
Clean database| `--clean`, `-c`Drops all the database objects that will be restored before restoring them.  
Add "IF EXISTS"| `--if-exists`Uses `DROP ... IF EXISTS` to drop objects when Clean database is enabled.  
Create database| `--create`, `-C`Creates a new database first and then restores into it. If Clean database is enabled, drops and recreates the target database before connecting to it.  
Data only| `--data-only`, `-a` Restores only the data, not the schema.  
Single transaction| `--single-transaction`, `-1`Performs the restore within a single transaction by wrapping it in `BEGIN` and `COMMIT`.  
  
For more information about export options, refer to the [pg_restore documentation](https://www.postgresql.org/docs/current/app-pgrestore.html).

![the Restore with psql dialog](https://resources.jetbrains.com/help/img/idea/2025.3/db_restore_with_psql.png)

Hover over the export option to see the command line arguments in a tooltip.

Item| Description  
---|---  
Where to run| Sets where to run the tool. You can either run it locally or in a Docker container.

  1. Locally
     * Path to executable: Defines the path to the psql executable on your machine.
     * Output result to: Defines the path to the output result on your local machine.
  2. In a Docker container This functionality relies on the [Docker](https://plugins.jetbrains.com/plugin/7724-docker) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. For more information, refer to [Open plugin settings](managing-plugins.html#open-plugin-settings). 
     * Server: Sets the server used to run the container.
     * Container: Sets the container to run the psql executable in.
     * Path to executable: Defines the path to the psql executable inside the container.If you use the IDE [Docker](https://plugins.jetbrains.com/plugin/7724-docker) plugin, type path to the psql executable inside the container (for example, `/usr/bin/mysqldump`). 

  
Options  
Database| `--dbname`Connect to the specified database and restore directly into it.[psql documentation.](https://www.postgresql.org/docs/17/app-psql.html#APP-PSQL-OPTION-DBNAME)  
Path to dump| `--file`Defines the path to the dump file on your machine.[psql documentation.](https://www.postgresql.org/docs/17/app-psql.html#APP-PSQL-OPTION-FILE)  
Single transaction| `--single-transaction`, `-1`Performs the restore within a single transaction by wrapping it in `BEGIN` and `COMMIT`.[psql documentation.](https://www.postgresql.org/docs/17/app-psql.html#APP-PSQL-OPTION-SINGLE-TRANSACTION)  
  
For more information about export options, refer to the [psql documentation](https://www.postgresql.org/docs/17/app-psql.html).
