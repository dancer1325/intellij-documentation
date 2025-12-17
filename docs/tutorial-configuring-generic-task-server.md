[//]: # (Source: https://www.jetbrains.com/help/idea/tutorial-configuring-generic-task-server.html)
[//]: # (Downloaded: 2025-12-17 20:04:40)

# Tutorial: Configure a generic task server

IntelliJ IDEA supports [integration with many task trackers](managing-tasks-and-context.html) out of the box. However, if you use a tracker that IntelliJ IDEA does not support yet, you can still integrate it configuring a so-called generic server.

This tutorial describes how to:

  * Connect to JIRA Cloud as a generic server.

  * Get the list of issues assigned to you.

  * For each issue, get its ID, title, description, date and time when the issue was created and updated.




Before you start configuring a connection to your tracker, note that IntelliJ IDEA:

  * Supports only services with REST API.

  * Supports either [Basic HTTP authentication](https://en.wikipedia.org/wiki/Basic_access_authentication) or sending preliminary requests to the server.

  * Supports GET and POST requests.

  * Does not support pagination in server responses.




### Enable the Task Management plugin

This functionality relies on the [Task Management](https://plugins.jetbrains.com/plugin/11545-task-management) plugin, which is bundled and enabled in IntelliJ IDEA by default. If the relevant features are not available, make sure that you did not disable the plugin. 

  1. Press `Ctrl+Alt+S` to open settings and then select Plugins.

  2. Open the Installed tab, find the Task Management plugin, and select the checkbox next to the plugin name.




### Specify server URL and credentials

  1. Press `Ctrl+Alt+S` to open settings and then select Tools | Tasks | Servers.

  2. Click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select Generic.

  3. On the General tab, specify the URL of your task tracker and connection credentials.

In the Username field, type your email address.

In the Password field, enter your [Atlassian API token](https://confluence.atlassian.com/cloud/api-tokens-938839638.html).

  4. Select the Use HTTP authentication checkbox at the bottom of the dialog.




### Configure the server settings

  1. Switch to the [Server Configuration](managing-tasks-and-context.html#server-configuration-tab-controls) tab.

Note that the Login URL field will be disabled, as you are using HTTP authentication.

  2. In the Tasks List URL, enter the URL for getting issues from the server. You can use variables or enter the full URL:

`{serverUrl}/rest/api/3/search/` or

`https://serverurl.atlassian.net/rest/api/3/search/`

The `{serverUrl}` is a variable that stands for the URL you have specified on the General tab.

  3. Add the `jql?fields=*all&jql={JQL_Query}` expression to your task list URL: `{serverUrl}/rest/api/3/search/jql?fields=*all&jql={JQL_Query}`.

You can use code completion in the Login URL, Task List URL and Single Task URL fields.

  4. Click Manage Template Variables at the bottom of the dialog to configure the `JQL_Query` variable.

  5. Click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and in the new field, specify the variable name `JQL_Query` and add its value `assignee = currentUser() AND resolution = unresolved`.

This will let you get unresolved issues assigned to you.

  6. Click OK. 




All variables specified in URL fields, except `{serverUrl}`, are encoded with `application/x-www-form-urlencoded` by default.

For more information about advanced searches, refer to [Advanced searching - fields reference](https://confluence.atlassian.com/jirasoftwarecloud/advanced-searching-fields-reference-764478339.html).

### Configure the response type and specify selectors

  1. In the Server Configuration dialog, select the JSON response type.

  2. Specify selectors in the table to get IDs and titles of issues and their description. You can also get the date and time when issues were created and updated:

     * tasks: `$.issues`

     * id: `key`

     * summary: `fields.summary`

     * description: `fields.description`

     * updated: `fields.updated`

     * created: `fields.created`

  3. Click Test to make sure all parameters are configured correctly.




### Upload issues from the server

  1. Click the task list and select Open Task. IntelliJ IDEA will load from the server all issues that match your configuration.

  2. Select the necessary issue from the list.

  3. Press `Ctrl+Q` to open issue description and make sure all required details are obtained.




14 October 2025

[Manage tasks](managing-tasks-and-context.html)[Contexts](contexts.html)
