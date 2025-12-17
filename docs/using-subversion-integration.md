[//]: # (Source: https://www.jetbrains.com/help/idea/using-subversion-integration.html)
[//]: # (Downloaded: 2025-12-17 20:05:47)

## Authenticate to Subversion

The Subversion server does not require user authentication on every request. When you use Subversion integration in IntelliJ IDEA, you only need to answer the authentication challenge of the server if it is required by the authentication and authorization policies. Upon successful authentication, your credentials are saved on disk, in <USER HOME>/.subversion_IDEA on macOS and Windows, and in ~/.subversion/auth/ on Unix systems .

When an authentication challenge comes from the server, the credentials are sought for in the disk cache; if the appropriate credentials are not found, or fail to authenticate, you are prompted to specify your login and password.

If necessary, you can opt to delete all credentials stored in the cache for the http, svn and ssh+svn protocols.

### To delete credentials from disk

  1. Press `Ctrl+Alt+S` to open settings and then select Version Control | Subversion.

  2. Select the Clear Auth Cache option.



