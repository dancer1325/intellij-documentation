[//]: # (Source: https://www.jetbrains.com/help/idea/http-client-reference.html)
[//]: # (Downloaded: 2025-12-17 19:29:01)

## Methods

### test

Creates a test with the name `testName` and body `func`. All tests are executed after the response handler script. Test results are displayed in the Tests tab of the Services tool window.

Parameter| Type| Description  
---|---|---  
testName| String| Test name  
func| function| JavaScript function to test an HTTP response  
  
### assert

Checks that the specified `condition` is `true`; throws an exception otherwise. The optional `message` parameter serves as an exception message.

Parameter| Type| Description  
---|---|---  
condition| boolean| The condition to check in the response  
message| String| The optional message to return in case the condition evaluates to false.  
  
### log

Prints `text` to the output of the response handler or pre-request script and then terminates the line.

Parameter| Type| Description  
---|---|---  
text| String| Text to be printed in the output of the response handler or pre-request script.  
  
### exit

Terminates execution of the response handler script.
