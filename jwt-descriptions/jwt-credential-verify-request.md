# JWT for [Credential Verify Request](../rest-api/credential-verify-request.md)
The JWT should encode a JSON object with the following params. NOTE: The JWT should be created using [our API](../rest-api/create-jwt.md) to automatically include some other required parameters.

-  ## `callbackUrl=[string]`
    The REST api of the verifier where to deliver the credential data.

-  ## `aud*=[string]`
    *\*Currently added later automatically and hardcoded, but will be required in the future.*

    The "aud" (audience) claim identifies the recipients that the JWT is intended for (currently hardcoded as `"ssi-service-provider"`).

-  ## `sub=[string]`
    The "sub" (subject) of the jwt. Should be `"credential-issue-request"`.

-  ## `jti*=[string]`
    *\*Currently added automatically (randomly generated) when [creating a jwt](../rest-api/create-jwt.md), but will be required in the future, maybe with a different name.*

    A unique identifier for the JWT within the context of the verifying party. Used by the verifying party to match a response with the corresponding request.

-  ## `type=[string]`
    The type of credential that is requested, as defined in the ssi service. This maps to the specific credential types of the different supported wallets.

## Example
```json
{
  "callbackUrl": "http://httpbin.org/get?response=",
  "aud": "ssi-service-provider",
  "sub": "credential-verify-request",
  "type": "FirstNameCredential"
}
```