[//]: # (Source: https://www.jetbrains.com/help/idea/settings-http-proxy.html)
[//]: # (Downloaded: 2025-12-17 20:01:10)

# HTTP Proxy

By default, IntelliJ IDEA uses your system proxy settings. Use this page to customize settings of an HTTP or SOCKS [proxy server](https://en.wikipedia.org/wiki/Proxy_server) for IntelliJ IDEA.

These settings affect the connections that IntelliJ IDEA establishes to download plugins, check license validity, synchronize IDE settings between instances, and perform other tasks for the IDE itself.

If you are not sure about the correct proxy settings in your organization, ask your system administrator for assistance.

![The HTTP Proxy page](https://resources.jetbrains.com/help/img/idea/2025.3/proxy_server_settings.png)

Item| Description  
---|---  
No proxy| Connect directly without a proxy.  
Auto-detect proxy settings| Use the system proxy settings (default behavior) or an automatically detected proxy auto-config (PAC) file.On Window and macOS, you can click System proxy settings to open the network proxy settings of your operating system.

  * Automatic proxy configuration URL: Manually specify the location of the PAC file.If the PAC file encoding is UTF-8 with BOM, it will not work. Make sure that the encoding is UTF-8 without BOM.
  * Clear Passwords: Clear the passwords for the specified proxy.

  
Manual proxy configuration| Specify proxy settings manually.

  * HTTP: Use an HTTP proxy.
  * SOCKS: Use a SOCKS proxy. For more information, refer to [Socket Secure protocol](http://en.wikipedia.org/wiki/SOCKS).
  * Host name: Specify the proxy hostname or IP address.
  * Port number: Specify the proxy port number.
  * No proxy for: Specify one or several host names or IP addresses for which no proxy should be specified. You can use an asterisk to denote a wildcard for any number of characters, and a comma to separate addresses.
  * Proxy authentication: Select this checkbox if your proxy requires authentication.
  * Login: Specify the user for connecting to the proxy.
  * Password: Specify the password associated with the user (login).
  * Remember: Select this checkbox if you want IntelliJ IDEA to remember the password between your sessions in the IDE. Otherwise, you will be asked to provide the password every time you launch IntelliJ IDEA when it first tries to connect to the proxy.

  
Check Connection| Click to check the proxy settings and, in the window that opens, enter a URL to check connection to it through the specified proxy server.  
  
07 April 2025

[Passwords](reference-ide-settings-password-safe.html)[Data Sharing](settings-usage-statistics.html)
