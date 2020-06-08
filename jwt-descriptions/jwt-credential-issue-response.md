# Credential Verify Response
The JWT returned to the callbackUrl specified in the [request](./jwt-credential-issue-request) encodes a JSON object with the following params. 

-  ## `requestId=[string]`
    Identifier matching the jti in the verify request.

-  ## `type=[string]`
    The type of credential that was issued, as defined in the ssi service. This maps to the specific credential types of the different supported wallets.

-  ## `status=[string]`
    The status of the issuing. Can be `success|error|cancelled`.

-  ## `connector=[string]`
    The connector that was used to store the issued credentials.

-  ## `iat=[number]`
    The "iat" (issued at) claim identifies the time at which the JWT was issued.  This claim can be used to determine the age of the JWT.

-  ## `aud*=[string]`
    The "aud" (audience) claim identifies the recipients that the JWT is intended for, this should match the identifier of the issuing party (i.e. the party that issued the credentials).

-  ## `iss*=[string]`
    The "iss" (issuer) claim identifies the principal that issued the JWT. When receiving a JWT from the ssi service, this should be the `"ssi-service-provider"`.

-  ## `sub=[string]`
    The "sub" (subject) of the jwt. Should be `"credential-issue-response"`.

## Example
```json
{
  "requestId": "Xks8zwLNk0A4",
  "type": "FirstNameCredential",
  "status": "success",
  "connector": "jolocom",
  "iat": 1590833726,
  "aud": "40d0fbd3-38a3-4a6e-8fe9-cfc56406749d",
  "iss": "ssi-service-provider",
  "sub": "credential-issue-response"
}
```