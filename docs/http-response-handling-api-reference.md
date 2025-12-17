[//]: # (Source: https://www.jetbrains.com/help/idea/http-response-handling-api-reference.html)
[//]: # (Downloaded: 2025-12-17 19:29:04)

# HTTP Response handling API reference

HTTP Response handler scripts are written in JavaScript ES6, with coding assistance and documentation handled by the bundled `HTTP Response Handler` library. The library exposes two objects to be used for composing response handler scripts:

  * [client](http-client-reference.html) stores the session metadata, which can be modified inside the script. The `client`'s state is preserved until you close IntelliJ IDEA.

  * [response](http-response-reference.html) holds information about the received response: its content type, status, response body, and so on.




17 June 2024

[OAuth 2.0 authorization](oauth-2-0-authorization.html)[HTTP Client reference](http-client-reference.html)
