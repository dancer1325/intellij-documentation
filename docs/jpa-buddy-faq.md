[//]: # (Source: https://www.jetbrains.com/help/idea/jpa-buddy-faq.html)
[//]: # (Downloaded: 2025-12-17 19:30:34)

## Why can't I find the JPA Buddy tabs/panels?

There are several reasons why you may not see the JPA Buddy panels.

**1\. You may not be in the correct file.**

JPA Buddy panels are only visible in certain files that JPA Buddy is familiar with, such as JPA entities, Spring Data JPA repositories, and Liquibase changelogs. This is because JPA Buddy panels are context-dependent. If you are not in a file that can be adjusted using JPA Designer, the corresponding panel might not be visible. To check if the JPA Designer panel is available, try opening a JPA entity. If it's not visible, move on to the next reason.

**2\. You may have Minimalistic Mode turned on.**

JPA Buddy has a [Minimalistic Mode](jpa-buddy-minimalistic-mode.html) that allows you to hide some or all panels according to your preference. If you accidentally turned on this mode, you can turn it off in the settings. To do so, go to Settings | Tools | JPA Buddy | Designer Settings and select the extensive option.

![extensive-mode.png](https://resources.jetbrains.com/help/img/idea/2025.3/extensive-mode.png)

Then, check if the panels are present (as described in point 1). Move to the next reason if JPA Buddy Panels still missing.

**3\. Your project may be missing necessary dependencies.**

As mentioned earlier, JPA Buddy displays its panels only when necessary. Therefore, if your project does not have any of [the libraries described in our documentation](jpa-buddy.html#dependencies), all JPA Buddy functionality will be disabled. To check if the necessary dependency exists in your project for JPA Buddy to work correctly, use the following method: Shift+Shift | Actions | JPA Structure.

![actions-jpa-structure.png](https://resources.jetbrains.com/help/img/idea/2025.3/actions-jpa-structure.png)

If you see the same, it means JPA Buddy is active, and the JPA Designer panel should be displayed if points 1 and 2 have been successful. If you are still unable to locate the panel, please refer to the last reason.

**4\. Something may have gone wrong with the plugin or IntelliJ IDEA.**

If none of the above points solve your problem, you can try the following steps:

  * Remove the plugin: go to Settings | Plugins | Installed Tab | Right Click on JPA Buddy | Uninstall

  * Clear the cache: go to File | Invalidate caches... | Tick all the boxes | Invalidate and Restart

  * Reinstall the plugin: go to Settings | Plugins | Marketplace | JPA Buddy and click Install.




If this still does not help, and you have the latest stable versions of [IntelliJ IDEA](https://www.jetbrains.com/idea/download/other.html) and [JPA Buddy](https://plugins.jetbrains.com/plugin/15075-jpa-buddy/versions), please create a ticket on [YouTrack](https://youtrack.jetbrains.com/issues/JPAB). When making the request, we would appreciate it if you could mention the version of IntelliJ IDEA, its type (CE or Ultimate), and the version of JPA Buddy.
