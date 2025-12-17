[//]: # (Source: https://www.jetbrains.com/help/idea/http-response-reference.html)
[//]: # (Downloaded: 2025-12-17 19:29:06)

## Response properties

The `response` object holds the information about a received HTTP Response (response content, headers, status, and so on) and provides access to the [headers](#headers-reference) and [contentType](#content-type-reference) nested objects.

Property| Description  
---|---  
`body` (string | [TextStreamResponse](#textstreamresponse_reference) | object)| Response content, which can be a string, a TextStreamResponse object, or a JSON object.  
`headers` ([ResponseHeaders](#headers-reference))| The [response headers storage object](#headers-reference).  
`status` (int)| Response status, for example, 200 or 404.  
`contentType` ([ContentType](#content-type-reference))| The [contentType object](#content-type-reference), which holds the data on the Content-Type response header value.
