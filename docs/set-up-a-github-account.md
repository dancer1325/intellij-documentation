[//]: # (Source: https://www.jetbrains.com/help/idea/set-up-a-github-account.html)
[//]: # (Downloaded: 2025-12-17 20:00:15)

## Add your GitHub account

To be able to retrieve data from a repository hosted on GitHub, or share your projects, you need to log in to your GitHub account in IntelliJ IDEA.

If you do not want to specify your credentials each time you [sync with a remote](sync-with-a-remote-repository.html), or [push](commit-and-push-changes.html) your commits, you can configure IntelliJ IDEA to save your account information (refer to [Configure a password policy](set-up-a-git-repository.html#password-policy)).

### Add an existing account by signing in to GitHub

  1. Press `Ctrl+Alt+S` to open settings and then select Version Control | GitHub.

  2. Click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) Add and select Log In via GitHub.

  3. Enter your GitHub credentials in the browser window that opens. If you have [two-factor authentication](https://blog.github.com/2013-09-03-two-factor-authentication/) enabled, you will be asked to enter a code that will be sent to you by SMS or through the mobile application.

The authorization is done using the OAuth 2.0.




### Add an existing account with a token

  1. Press `Ctrl+Alt+S` to open settings and then select Version Control | GitHub.

  2. Click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) Add and select Log In with Token.

  3. Do one of the following:

     * If you already have a token, insert it in the Add GitHub Account dialog window:

![Adding GitHub account with token](https://resources.jetbrains.com/help/img/idea/2025.3/add_github_account.png)
     * If you want to obtain a new token, click Generate.

Enter your GitHub credentials in the browser window that opens. If you have [two-factor authentication](https://blog.github.com/2013-09-03-two-factor-authentication/) enabled, you will be asked to enter a code that will be sent to you by SMS or through the mobile application.

In the token generation page, make sure that the repo, the gist and the read:org scopes are enabled (refer to [Understanding scopes](https://developer.github.com/apps/building-oauth-apps/understanding-scopes-for-oauth-apps/)).

Click Generate token, copy the token, and paste it into the Add GitHub Account dialog window.

  4. Click Add Account.




See [Creating a personal access token](https://help.github.com/en/articles/creating-a-personal-access-token-for-the-command-line) for more details on GitHub tokens.

### Log in to a GitHub Enterprise account

  1. Press `Ctrl+Alt+S` to open settings and then select Version Control | GitHub.

  2. Click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) Add and select Log In to GitHub Enterprise.

  3. In the Server field, enter the URL of your GitHub Enterprise server. For example, `github.com` for GitHub Enterprise Cloud, `example.ghe.com` for GitHub Enterprise Cloud (with Data Residency), or the URL of the self-hosting server that your company uses.

  4. Do one of the following:

     * If you already have a token, insert it in the Add GitHub Account dialog window:

![Adding GitHub Enterprise account with token](https://resources.jetbrains.com/help/img/idea/2025.3/gh_enterprise_server.png)
     * If you want to obtain a new token, click Generate.

Enter your GitHub credentials in the browser window that opens. If you have [two-factor authentication](https://blog.github.com/2013-09-03-two-factor-authentication/) enabled, you will be asked to enter a code that will be sent to you by SMS or through the mobile application.

In the token generation page, make sure that the repo, the gist and the read:org scopes are enabled (refer to [Understanding scopes](https://developer.github.com/apps/building-oauth-apps/understanding-scopes-for-oauth-apps/)).

Click Generate token, copy the token, and paste it into the Add GitHub Account dialog window.

  5. Click Add Account.




### Update an expired token

  1. When your token expires, you see the following warning when trying to push changes to the GitHub repository:

![Expired token warning](https://resources.jetbrains.com/help/img/idea/2025.3/ws_expired_token.png)

Click Use Token.

  2. Do one of the following:

     * If you already have a token, insert it in the Log In to GitHub dialog window:

![Adding GitHub account with token](https://resources.jetbrains.com/help/img/idea/2025.3/update_gh_token.png)
     * If you want to obtain a new token, click Generate.

Enter your GitHub credentials in the browser window that opens. If you have [two-factor authentication](https://blog.github.com/2013-09-03-two-factor-authentication/) enabled, you will be asked to enter a code that will be sent to you by SMS or through the mobile application.

In the token generation page, make sure that the repo, the gist and the read:org scopes are enabled (refer to [Understanding scopes](https://developer.github.com/apps/building-oauth-apps/understanding-scopes-for-oauth-apps/)).

Click Generate token, copy the token, and paste it into the Log In to GitHub dialog window.

  3. Click Log In




### Create a new GitHub account

  1. Press `Ctrl+Alt+S` to open settings and then select Version Control | GitHub.

  2. Click ![the Add button](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) Add and select Log In via GitHub.

  3. In the browser window that opens, click Create an account and complete the registration process on GitHub.

  4. Return to the IntelliJ IDEA settings, click Cancel, and then repeat steps 2 and 3.

  5. Click Authorize JetBrains in your browser.




### Manage multiple GitHub accounts

You can use multiple GitHub accounts in IntelliJ IDEA: for example, a personal account to work on an open-source project, and a corporate account for your main job.

  1. Press `Ctrl+Alt+S` to open settings and then select Version Control | GitHub.

  2. Use ![add icon](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.add.svg) Add to add as many accounts as you need.

  3. (Optional) To set an account as a default one for the current project, select it and click ![the Check button](https://resources.jetbrains.com/help/img/idea/2025.3/app.actions.checked.svg) Set as Default. If a default account is set, IntelliJ IDEA will not ask you to select an account you want to use when you [share your project on GitHub](manage-projects-hosted-on-github.html#share-on-GitHub), [rebase a fork](fork-github-projects.html#rebase-fork), [create a pull request](create-and-merge-github-pull-requests.html#create-pull-request), or [create a gist](share-code-with-gists.html).



