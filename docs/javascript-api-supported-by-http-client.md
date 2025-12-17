[//]: # (Source: https://www.jetbrains.com/help/idea/javascript-api-supported-by-http-client.html)
[//]: # (Downloaded: 2025-12-17 19:30:19)

## console.log

The HTTP Client supports the `console.log()` method to print the text value (or multiple values separated by commas) to the output of the response handler or pre-request handler scripts. You can also use [client.log](http-client-reference.html) for the same purpose. Example:

GET example.org > {% console.log(response.status) %} 

You can also pass a JavaScript object (for example, `console.log(response.body)`), and it will be displayed in the output in JSON format with proper syntax highlighting.
