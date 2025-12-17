[//]: # (Source: https://www.jetbrains.com/help/idea/set-up-a-gitlab-account.html)
[//]: # (Downloaded: 2025-12-17 20:00:16)

## Manage GitLab accounts

To retrieve data from a project hosted on GitLab or share your projects, you need to log in to your GitLab account in IntelliJ IDEA.

### Log in to GitLab

  1. Press `Ctrl+Alt+S` to open settings and then select Version Control | GitLab.

  2. Click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg). The Log In with Access Token dialog opens: 

![Log In with Access token dialog](https://resources.jetbrains.com/help/img/idea/2025.3/log_in_with_access_token.png)
  3. In the dialog, do one of the following:

     * If you already have a token, insert it in the Token field.

     * If you have no token, click Generate.

In the token generation page that opens, make sure that the `api` and `read_user` scopes are selected.

Click Create personal access token, copy the token, and paste it into the Log In with Access Token dialog window.

  4. Click Log In.




See [Personal access tokens](https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html) for more details on GitLab tokens.

### Manage multiple GitLab accounts

You can use multiple GitLab accounts in IntelliJ IDEA: for example, a personal account to work on an open-source project, and a corporate account for your main job.

  1. Press `Ctrl+Alt+S` to open settings and then select Version Control | GitLab.

  2. Use the ![add icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) button to add as many accounts as you need.

  3. To set an account as the default one for the current project, select it and click ![the Check button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.checked.svg). 

![Check button that sets the default account](https://resources.jetbrains.com/help/img/idea/2025.3/set_default_account_gitlab.png)


