# Register Credential Type (Jolocom)
Register a new credential type for issuing and verifying with the Jolocom app.

- ## Url
  `/api/connectors/jolocom`

- ## Method
  `POST`

- ## URL Params
  None

- ## Body Params
  *JSON object with the following params:*
  ### Required
  `claimInterface=[object]`

  `context=[object]`

  `name=[string]`
  
  `type=[string]`

  ### Example:
  ```json
  {
      "claimInterface": {
          "firstName": ""
      },
      "context": [
          {
              "firstName": "https://schema.org/givenName"
          }
      ],
      "name": "First Name Credential",
      "type": "FirstNameCredential"
  }
  ```

- ## Success Response
  - ### Code
    201 Created
    ### Content
    ```json
    {
        "type": "FirstNameCredential",
        "name": "First Name Credential",
        "claimInterface": {
            "firstName": ""
        },
        "context": [
            {
                "firstName": "https://schema.org/givenName"
            }
        ],
        "id": 1
    }
    ```

- ## Error Response
  - ### Code
    400 Bad Request
    ### Content
    ```json
    {
      "statusCode": 400,
      "message": [
          "type should not be empty",
          "type must be a string",
          "context must be an array",
          "claimInterface must be a non-empty object"
      ],
      "error": "Bad Request"
    }
    ```