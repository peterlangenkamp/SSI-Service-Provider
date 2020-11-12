# Documentation for using the ssi service

While the SSI service can be used through our [utils page](https://service.essif-lab-ssi.dev.grnet.gr/utils) (described [here](./service-instructions/utils-overview.md)), for practical use it can be interacted with directly through the available APIs.

## API description
The files below provide a description of the REST api for interacting with the ssi service.

- [Create JWT](./rest-api/create-jwt.md)
- [Credential Issue Request](./rest-api/credential-issue-request.md)
- [Credential Verify Request](./rest-api/credential-verify-request.md)
- [Register Credential Type (Jolocom)](./rest-api/register-credential-type-jolocom.md)
- [Register Organization's Credential Types](./rest-api/register-organizations-credential-type.md)
- [Register Organization](./rest-api/register-organization.md)
- [Registered Credential Type (Jolocom)](./rest-api/registered-credential-types-jolocom.md)
- [Registered Organization's Credential Types](./rest-api/registered-organizations-credential-types.md)
- [Registered Organizations](./rest-api/registered-organizations.md)

For a description of the content of the different jwt tokens, refer to

- [Issue Request](./jwt-descriptions/jwt-credential-issue-request)
- [Issue Response](./jwt-descriptions/jwt-credential-issue-response)
- [Verify Request](./jwt-descriptions/jwt-credential-verify-request)
- [Verify Response](./jwt-descriptions/jwt-credential-verify-request)
- [Create JWT](./jwt-descriptions/response-jwt-create-jwt)

## Connecting a new wallet app

Interested in connecting to our service? Please let us know by sending an email to [Peter Langenkamp](mailto:peter.langenkamp@tno.nl&cc=michiel.stornebrink@tno.nl).