[//]: # (Source: https://www.jetbrains.com/help/idea/test-management-systems.html)
[//]: # (Downloaded: 2025-12-17 20:04:11)

## Connect to a remote TMS

While you cannot change test data in a remote TMS, you can still benefit from the integration by linking test data and code. For example, this is useful when searching for [outdated tests](#find-outdated) or [candidates for automation](#find-candidates-for-automation).

  1. Press `Ctrl+Alt+S` to open settings and then select Tools | TMS.

  2. In Remote Connections, click Add and select TestRail.

Currently, only TestRail 6.7 or later is supported.

Other test management systems will be added in future releases. Feel free to vote for the corresponding requests:

     * [IDEA-268401 - TestLink](https://youtrack.jetbrains.com/issue/IDEA-268401)

     * [IDEA-268399 - Xray for Jira](https://youtrack.jetbrains.com/issue/IDEA-268399)

     * [IDEA-268393 - Zephyr](https://youtrack.jetbrains.com/issue/IDEA-268393)

  3. Specify:

     * URL, including the protocol prefix, for example, `https://mytms.testrail.net`

     * login and password for the remote TMS

  4. Optionally, [configure a proxy](settings-http-proxy.html).

  5. After you have entered valid credentials, specify the test project within the TMS.



