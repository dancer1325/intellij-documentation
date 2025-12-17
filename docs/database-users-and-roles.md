[//]: # (Source: https://www.jetbrains.com/help/idea/database-users-and-roles.html)
[//]: # (Downloaded: 2025-12-17 19:24:06)

# Users and roles

Users and roles functionality and options depend on the database vendor.

If the information you are looking for is missing in this topic, [contact the Support team](getting-help.html#contact-support) and provide them with the details of your database.

Different databases use concepts of users and roles to manage the permissions in your databases. Both of them are used for access control and define a set of permissions. In some databases, a role can be a user that has the login right.

Settings in the Create and Modify dialogs vary depending on the database vendor. Consult with the documentation of your database vendor for the list of settings and type of concept the database uses for access control.

Users and roles ( ![User](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.user.svg) and ![Role](https://resources.jetbrains.com/help/img/idea/2025.3/database-plugin.icons.expui.role.svg)) can be found in the Database tool window under Server Objects.

  * For the reference on other node and object icons, refer to the [Data sources and their elements](database-tool-window.html#icons-for-data-sources-and-their-elements) chapter of [Database tool window](database-tool-window.html) topic.

  * Hide, sort, filter, and group tree objects using the tree objects view options in the [View Options](database-tool-window.html#view_options) menu.


![Users and roles in Database](https://resources.jetbrains.com/help/img/idea/2025.3/database_object_user_role.png)

Users and roles are not supported for the following database vendors: Google BigQuery, Couchbase Query Service, HSQLDB, MongoDB, Redis.

### Create a user or a role

  1. In the Database tool window, right-click a data source node and navigate to New | User or New | Role. 

For some databases, you need to specify a database where you want to create a role or a user. In this case, you must expand the data source tree to the database node, right-click the database node and select New | User or New | Role.

  2. In the Create dialog that opens, enter the name of your user or role in the Name field.

  3. Select and specify the necessary database settings.

  4. In the Preview pane, you can view and change the generated SQL code.

  5. Click OK to add your user role.


![Create a user](https://resources.jetbrains.com/help/img/idea/2025.3/db_create_user_or_role.png)

### Grant permissions

You can grant a user and a role permissions for database objects.

For other database objects, you can configure the permissions that each grantee has for the object, and the list of grantees. To do that, open the Modify dialog for the object and use the Grants pane.

  1. In the Database tool window, right-click a user or a role and select Modify Role.

  2. In the Grants pane of the Modify dialog, click the Add button (![the Add icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg)).

You can use auto-completion for database objects.

  3. Click the grant field, from the drop-down near each permission, select Grant or Grant with option. The Grant with option permission means that a user can grant to or revoke from other users those permissions.

![GRANT permissions for users](https://resources.jetbrains.com/help/img/idea/2025.3/db_grant_permissions_for_users.png)



28 October 2025

[Views](views.html)[Virtual foreign keys](virtual-foreign-keys.html)
