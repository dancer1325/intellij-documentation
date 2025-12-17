[//]: # (Source: https://www.jetbrains.com/help/idea/ssl-certificates.html)
[//]: # (Downloaded: 2025-12-17 20:03:16)

## How it works under the hood

Under Linux, all certificates in `.crt` (PEM) format from the following locations are imported:

  * `/etc/ssl/certs/*`

  * `/etc/pki/tls/certs/*`

  * `/system/etc/security/cacerts/*`

  * `/etc/ssl/certs/ca-certificates.crt`

  * `/etc/pki/tls/certs/ca-bundle.crt`

  * `/etc/ssl/ca-bundle.pem`

  * `/etc/pki/tls/cacert.pem`

  * `/etc/pki/ca-trust/extracted/pem/tls-ca-bundle.pem`

  * `/etc/ssl/cert.pem`




For more information, refer to the [JetBrains Linux Trusted Certificates](https://github.com/JetBrains/jvm-native-trusted-roots/blob/trunk/src/main/java/org/jetbrains/nativecerts/linux/LinuxTrustedCertificatesUtil.java) library.

Under macOS X, the code calls system functions to get system-wide and user-specific custom trusted certificates.

For more information, refer to the [JetBrains macOS Trusted Certificates](https://github.com/JetBrains/jvm-native-trusted-roots/blob/trunk/src/main/java/org/jetbrains/nativecerts/mac/SecurityFrameworkUtil.java) library.

Under Windows, the code calls system functions to get system-wide, user-specific, or group-policy distributed trusted certificates.

For more information, refer to the [JetBrains Windows Trusted Certificates](https://github.com/JetBrains/jvm-native-trusted-roots/blob/trunk/src/main/java/org/jetbrains/nativecerts/win32/Crypt32Ext.java) library.
