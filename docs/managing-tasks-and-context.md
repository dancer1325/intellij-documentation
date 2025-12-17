[//]: # (Source: https://www.jetbrains.com/help/idea/managing-tasks-and-context.html)
[//]: # (Downloaded: 2025-12-17 19:31:54)

## Configure integration with issue trackers

IntelliJ IDEA supports integration with:

  * [Jira](https://www.atlassian.com/software/jira)

  * [YouTrack](https://www.jetbrains.com/youtrack/)

  * [Lighthouse](https://lighthouseapp.com/)

  * [PivotalTracker](https://www.pivotaltracker.com/)

  * [Redmine](https://www.redmine.org/)

  * [Trac](https://trac.edgewall.org/)

  * [FogBugz](https://www.fogbugz.com/)

  * [Mantis](https://www.mantisbt.org/)

  * [Asana](https://asana.com/)

  * [Assembla](https://www.assembla.com/features/bug-tracking)

  * [Sprint.ly](https://sprint.ly/)

  * [Trello](https://trello.com/)

  * [GitLab](https://about.gitlab.com/)

  * [Bugzilla](https://www.bugzilla.org/)

  * [GitHub](https://github.com/)

  * [Generic server](tutorial-configuring-generic-task-server.html)




### Connect the IDE to your tracker

  1. In the Settings dialog `Ctrl+Alt+S`, select Tools | Tasks | Servers.

  2. Click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) and select the necessary issue tracker from the list.

  3. Enter connection details. Note that settings differ depending on your issue tracker.

Normally, you have to specify the server URL and connection credentials: Username and Password.

In some cases, you need to enter an API token instead of your password.

For example, if you're connecting your IDE to YouTrack, the Password field is replaced with Token. Learn more from [Manage Permanent Tokens](https://www.jetbrains.com/help/youtrack/standalone/Manage-Permanent-Token.html).

For Jira, enable the Use personal access token option to use a [token](https://confluence.atlassian.com/enterprise/using-personal-access-tokens-1026032365.html) instead of your user name and password.

  4. Select the Share URL option to allow access to the server for other members of your team. When this option is enabled, a server URL and its type are saved to the .idea/misc.xml file, which can be shared between development team members through version control.

  5. Click Proxy settings if you want to access the server using a proxy server. You can find more information on proxy settings in the [HTTP Proxy](settings-http-proxy.html) section.

![Setting on the General tab of the Servers page](https://resources.jetbrains.com/help/img/idea/2025.3/tasks-connect-server.png)
  6. On the Commit Message tab, you can enable adding a commit message for a changelist and configure a message template.

  7. On the Server Configuration tab, configure advanced [parameters](#server-configuration-tab-controls) for connecting to your issue tracker.

This tab is only available for some trackers (for example, for [trackers that are not supported out of the box](tutorial-configuring-generic-task-server.html)).

Code completion is available in the fields on this tab.




### Server Configuration tab parameters

Item| Description  
---|---  
Login URL| The resource for authentication. The IDE sends requests to this resource every time before retrieving the list of issues from the server, for example: `{serverUrl}/rest/user/login?login={username}&password={password}`.The field is disabled if you have selected the Use HTTP authentication checkbox on the General tab.  
Tasks List URL| The resource for retrieving the list of issues from the server, for example: `{serverUrl}/rest/api/2/search`.  
Single Task URL| The resource for retrieving detailed information about an issue by its ID, for example: `{serverUrl}/rest/api/2/issue/{id}`.This field is optional unless you select the Each task in separate request checkbox.  
GET or POST| Select the necessary type of HTTP requests.  
Each task in separate request| Enabling this option allows the IDE to send several requests to retrieve the list of issues with their IDs first and then to get detailed information on each issue separately using the resource specified in the Single Task URL field.This option is for issue trackers with restricted REST APIs that cannot send all the required information in a single response.  
Response type| Select the format in which your issue tracker responses: XML for XPath, JSON for [JSONPath](https://goessner.net/articles/JsonPath/), or Text for regular expressions.  
The table of selectors| Selectors allow you to specify which information about an issue is going to be retrieved from the server response.  
tasks| The path to the list of issues in the server response. This field is mandatory.  
id| The path to the issue ID in the server response. This field is mandatory.  
summary| The path to the issue title in the server response. This field is mandatory.  
  
For more information about configuring these parameters, refer to [Tutorial: Configure a generic task server](tutorial-configuring-generic-task-server.html).

### Specify additional integration options

  1. In the Settings dialog `Ctrl+Alt+S`, select Tools | Tasks.

  2. Configure the necessary options:

     * Changelist name format: when you open or create a new task, IntelliJ IDEA [prompts you to create a new changelist](#changelist) associated with this task. In this field, you can specify a template that will be used for generating names for new changelists.

Click ![the Add placeholder button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) to select placeholders from the list.

     * Feature branch name format: when you create or open a new task, IntelliJ IDEA prompts you to create a new feature branch. In this field, you can configure the template for generating names of new feature branches.

Click ![the Add placeholder button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) to select placeholders from the list.

Use the Lowercased and Replace spaces with options to configure prompted feature branch names.

These settings are useful if your IDE is integrated with an issue tracker. For example, the DSGN-0001 Add new icon task name is going to be converted to the dsgn-0001add-new-icon feature branch name.

You can always modify a feature branch name before creating it if the generated name doesn't work for you.

     * Task history length: the number of tasks that IntelliJ IDEA stores.

     * Save context on commit: every time you commit changes, IntelliJ IDEA creates a new closed local task that keeps files, bookmarks, and breakpoints that you have worked with. This way, you can quickly restore all tabs associated with the task any time in the future.

     * Enable issue cache: optimize synchronization between IntelliJ IDEA and your issue tracker. Synchronization is especially recommended if you work with "slow" issue tracking systems.

IntelliJ IDEA caches the list of issues loaded from the tracker and updates them repeatedly. You can specify how many issues should be cached and how often IntelliJ IDEA should update information about them.

![Task settings](https://resources.jetbrains.com/help/img/idea/2025.3/tasks_settings.png)


