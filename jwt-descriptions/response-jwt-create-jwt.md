# JWT Response to [Create JWT](../rest-api/create-jwt.md)
The JWT response adds the following params.

-  ## `iat=[number]`
    The "iat" (issued at) claim identifies the time at which the JWT was issued.  This claim can be used to determine the age of the JWT.

-  ## `aud=[string]`
    The "aud" (audience) claim identifies the recipients that the JWT is intended for.

-  ## `iss=[string]`
    The "iss" (issuer) claim identifies the principal that issued the JWT.

-  ## `jti=[string]`
    The "jti" (JWT ID) claim provides a unique identifier for the JWT.

## Example:
### Submitted
  ```json
  {
    "type": "FirstNameCredential",
    "callbackUrl": "https://jwt.io/"
  }
  ```
### Decoded response
```json
{
    "type": "FirstNameCredential",
    "callbackUrl": "https://jwt.io/",
    "iat": 1590824876,
    "aud": "ssi-service-provider",
    "iss": "40d0fbd3-38a3-4a6e-8fe9-cfc56406749d",
    "jti": "DvzGJEoEuhpi"
}
```