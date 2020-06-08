# Registered Credential Types (Jolocom)
Retrieve a list with the credential types that are registered for Jolocom.

- ## Url
  `/api/connectors/jolocom`

- ## Method
  `GET`

- ## URL Params
  None

- ## Body Params
  None

- ## Success Response
  - ### Code
    200 OK
    ### Content
    ```json
    [
        {
            "id": 1,
            "type": "FirstNameCredential",
            "name": "First Name Credential",
            "context": [
                {
                    "firstName": "https://schema.org/givenName"
                }
            ],
            "claimInterface": {
                "firstName": ""
            }
        },
        {
            ...
        }
    ]
    ```

- ## Error Response
  \-