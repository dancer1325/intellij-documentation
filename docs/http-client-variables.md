[//]: # (Source: https://www.jetbrains.com/help/idea/http-client-variables.html)
[//]: # (Downloaded: 2025-12-17 19:29:03)

## Variable types

There are several types of variables in the HTTP Client. They differ by scope and priority; if variable names conflict, the value of the variable higher on the list will be used.

  * [Environment variables](#environment-variables) defined in dedicated environment files and available in any .http file. In case of a name conflict, public variables take precedence over private ones.

Access using `client.variables.environment` or `request.environment`.

  * [Global variables](http-client-reference.html#global-variables-storage-reference) defined in [response handler and pre-request scripts](http-client-in-product-code-editor.html#using-response-handler-scripts).

Access using `client.variables.global` or `client.global`.

  * [In-place variables](#in-place-variables) defined in .http files and available within the same files only.

Access using `client.variables.file`.

  * [Per-request variables](#per_request_variables) defined before a request and available only within the single request that follows.

Access using `client.variables.request` or `request.variables`.

  * Additionally, the HTTP Client provides [built-in dynamic variables](#dynamic-variables) with dynamically generated values. Such variables have reserved names.




To simplify working with different types of variables, the HTTP Client provides a single access point `client.variables`. You can use it in pre-request and response-handler scripts to access all variable scopes. The already existing access points, like `client.global`, `request.environment`, and `request.variables` are also preserved.
