# api route description

 ## METHOD ROUTE PATH
 `POST /credentials/:id/reveal`

 ## Description
Reveal and return the decrypted password for a given credential

 ## Authorization
 - Required
 - Header :
 ```http
 Authorization: Bearer <JWT>
 ```

 ## Request
 ```http
 Content-type:application/json
 Authorization:Bearer <JWT>
 ```

 ## Body
 ```json
 {
 "field":"value"
 }
 ```

 ## Example: 
 ```json
 {
 "unlock_key":"userInputUnlockKey"
 }
 ```

 ## Response
 200 OK:
 ```json
 {
 "password":"decryptedPlainPassword"
 }
 ```

 4xx/5xx Errors:
|Status | Description | Example |
|:------|:------------------------------|:-------------------------------------|
|400    |Missing required field         |```{"error":"unlock_key required"}``` |
|401    |Invalid unlock key             |```{"error":"invalid unlock_key"}```  |
|403    |Unauthorized access to resource|```{"error":"Forbidden"}```           |
|500    |Internal server error          |```{"error":"Something went wrong"}```|

 ## Validation Rules
-`unlock_key`: required, string, non-empty
