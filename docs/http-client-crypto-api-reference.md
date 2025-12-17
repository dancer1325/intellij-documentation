[//]: # (Source: https://www.jetbrains.com/help/idea/http-client-crypto-api-reference.html)
[//]: # (Downloaded: 2025-12-17 19:28:58)

## Hash methods

Method| Parameters| Description  
---|---|---  
`updateWithText`| `textInput` (string)`encoding` (string): the encoding of `textInput`. Default is `UTF8`.| Updates a string to be transformed to a hash.  
`updateWithHex`| `hexInput` (string)| Updates a hexadecimal string to be transformed to a hash.  
`updateWithBase64`| `base64Input` (string)`urlSafe` (boolean): enter `true` if the string is encoded using the URL-safe variant of Base64.| Updates a Base64 string to be transformed to a hash.  
`digest().toHex()`| —| Generates a hash and convert it to the hexadecimal format.  
`digest().toBase64()`| `urlSafe` (boolean): enter `true` if you want to use the URL-safe variant of Base64| Generates a hash and convert it to the Base64 format.
