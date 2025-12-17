[//]: # (Source: https://www.jetbrains.com/help/idea/http-response-handling-examples.html)
[//]: # (Downloaded: 2025-12-17 19:29:05)

## Checking response headers, body, and content type

In this example, we'll create several tests to verify the following:

  * The request is executed successfully, that is, the response status is 200.

  * Headers are received within the response body.

  * The response's content type is application/json.




To create a test, we call the `test` method of the [client](http-client-reference.html) object. Inside the test, we can assert a specific condition by calling the `assert` method of the `client` object and refer to various properties of the [response](http-response-reference.html) object to validate them.

### Check response status, headers, and content-type GET https://httpbin.org/get > {% client.test("Request executed successfully", function() { client.assert(response.status === 200, "Response status is not 200"); }); client.test("Headers option exists", function() { client.assert(response.body.hasOwnProperty("headers"), "Cannot find 'headers' option in response"); }); client.test("Response content-type is json", function() { var type = response.contentType.mimeType; client.assert(type === "application/json", "Expected 'application/json' but received '" + type + "'"); }); %} 
