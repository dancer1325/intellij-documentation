[//]: # (Source: https://www.jetbrains.com/help/idea/exploring-http-syntax.html)
[//]: # (Downloaded: 2025-12-17 19:26:01)

## Handle the response

You can handle the response using JavaScript. Type the `>` character after the request and specify the path and name of the JavaScript file or put the response handler script code wrapped in `{% ... %}`.

GET https://httpbin.org/get > /path/to/responseHandler.js 

GET https://httpbin.org/get > {% client.global.set("my_cookie", response.headers.valuesOf("Set-Cookie")[0]); %} 

For more information, refer to [HTTP Response handling API reference](http-response-handling-api-reference.html).
