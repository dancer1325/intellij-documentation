[//]: # (Source: https://www.jetbrains.com/help/idea/register.html)
[//]: # (Downloaded: 2025-12-17 19:57:05)

## Trial and subscription

When you start IntelliJ IDEA for the first time, you will be automatically granted a free 30-day trial. You can check the remaining number of days, by clicking Trial in the right upper corner of your IDE.

If a trial period ends or your subscription expires, you will still have access to IntelliJ IDEA with a free feature set.

After the trial version expires, you need to buy and register a commercial license to continue using the Ultimate feature set. A new trial period will be available for the next major version of IntelliJ IDEA.

### Subscribe to IntelliJ IDEA

For more information on our licensing model, refer to the [Licensing and Purchasing FAQ](https://sales.jetbrains.com/hc/en-gb).

  1. Select Help | Register from the main menu or click ![Options Menu](https://resources.jetbrains.com/help/img/idea/2025.3/app.expui.general.settings.svg) |Manage Subscriptions on the Welcome screen to open the Manage Subscriptions dialog.

![IntelliJ IDEA: Licenses dialog](https://resources.jetbrains.com/help/img/idea/2025.3/ij_register.png)
  2. Choose how you want to register IntelliJ IDEA or a plugin that requires a license:

Log in to your [JetBrains Account](https://account.jetbrains.com/login) and get licenses that you have purchased.

If you don't have a JetBrains Account yet, click Register.

![Activate IntelliJ IDEA license with a JB Account](https://resources.jetbrains.com/help/img/idea/2025.3/ij_activate_license.png)

IntelliJ IDEA automatically shows the list of your licenses and their details like expiration date and identifier. Click Activate to start using your license. 

If your license is not shown on the list, click Refresh license list.

Provide an activation code and click Activate.

![Activate IntelliJ IDEA license with an activation code](https://resources.jetbrains.com/help/img/idea/2025.3/ij_activate_license_activation_code.png)

When purchasing a product license, you receive a code for its offline activation. You can always download available activation codes from your [JetBrains Account](https://account.jetbrains.com/licenses).

Register using the [Floating License Server](https://www.jetbrains.com/help/license_server/Activating_license.html) or [License Vault](https://www.jetbrains.com/help/license-vault-cloud/Activating_a_license.html#to-activate-a-license).

![Activate IntelliJ IDEA license with a license server](https://resources.jetbrains.com/help/img/idea/2025.3/ij_activate_license_server.png)

When performing a silent installation or managing IntelliJ IDEA installations on multiple machines, you can set the `JETBRAINS_LICENSE_SERVER` environment variable to point to the URL of the Floating License Server or License Vault.

Alternatively, you can set the URL of the Floating License Server or License Vault by adding the `-DJETBRAINS_LICENSE_SERVER` [JVM option](tuning-the-ide.html#configure-jvm-options).

IntelliJ IDEA detects the system proxy URL during initial startup and uses it for connecting to the JetBrains Account, Floating License Server, and License Vault. To override the URL of the system proxy, add the `-Djba.http.proxy` [JVM option](tuning-the-ide.html#configure-jvm-options). Specify the proxy URL as the host address and optional port number: `proxy-host[:proxy-port]`. For example: `-Djba.http.proxy=http://my-proxy.com:4321`.

If you want to disable proxy detection entirely and always connect directly, set the property to `-Djba.http.proxy=direct`.



