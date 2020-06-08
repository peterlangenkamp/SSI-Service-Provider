# JWT for [Credential Issue Request](../rest-api/credential-issue-request.md)
The JWT should encode a JSON object with the following params. NOTE: The JWT should be created using [our API](../rest-api/create-jwt.md) to automatically include some other required parameters.

-  ## `callbackUrl=[string]`
    The REST api of the verifier where to deliver the credential data.

-  ## `aud*=[string]`
    *\*Currently added later automatically and hardcoded, but will be required in the future.*

    The intended audience for the jwt (currently hardcoded as `"ssi-service-provider"`).

-  ## `sub=[string]`
    The type of jwt, should be `"credential-issue-request"`.

-  ## `jti*=[string]`
    *\*Currently added automatically (randomly generated) when [creating a jwt](../rest-api/create-jwt.md), but may be required in the future, possibly with a different name.*

    A unique identifier for the JWT within the context of the issuing party, Used by the issuing party to match a response with the corresponding request.

-  ## `type=[string]`
    The type of credential to be issued, as defined in the ssi service. This maps to the specific credential types of the different supported wallets.

-  ## `data=[object]`
    Object containing the actual data to be issued. The content of this object should match the schema of the credential type.

## Example
```json
{
  "callbackUrl": "http://httpbin.org/get?response=",
  "aud": "ssi-service-provider",
  "sub": "credential-issue-request",
  "type": "FirstNameCredential",
  "data": {
    "firstName": "John"
  }
}
```