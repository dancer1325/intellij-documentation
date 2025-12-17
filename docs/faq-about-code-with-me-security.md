[//]: # (Source: https://www.jetbrains.com/help/idea/faq-about-code-with-me-security.html)
[//]: # (Downloaded: 2025-12-17 19:26:41)

## How and what data is going through JetBrains' servers?

Your project /solution data is going through JetBrains' servers end-to-end encrypted. The end-to-end encryption is secure only when a host and a guest verify that the security code matches on both ends. Otherwise, the end-to-end encryption is susceptible to MitM.

Local IP addresses, project name, and username are shared without encryption as they are used for letting JetBrains establish a session between a host and a guest. When initiating a new Code With Me session, the host communicates with JetBrains server over TLS1.2+.

Code With Me communicates through an [open source distributed protocol](https://github.com/JetBrains/rd) created by JetBrains and uses TLS 1.3 for end-to-end encryption.

If you don't want your data to go via JetBrains servers, you can configure the [on-premises servers](https://www.jetbrains.com/help/cwm/code-with-me-quick-setup.html).
