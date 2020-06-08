# Register Organization's Credential Types
Register the mapping of the general credential type to those of different wallets (e.g. Irma and Jolocom)

- ## Url
  `/api/types`

- ## Method
  `POST`

- ## URL Params
  None

- ## Body Params
  *JSON object with the following params:*
  ### Required
  `organizationId=[number]`

  `type=[string]`

  ### Optional
  `irmaType=[string]`
  
  `jolocomCredentialTypeId=[number]`

  ### Example:
  ```json
  {
    "irmaType": "irma-demo.MijnOverheid.fullName",
    "jolocomCredentialTypeId": 1,
    "organizationId": 1,
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
      "irmaType": "irma-demo.MijnOverheid.fullName",
      "organization": {
          "id": 1,
          "name": "New org",
          "sharedSecret": "76cd77019a62b7c1b0a665bdfec941debbff7c5360f65541016e04db12cbdac8",
          "uuid": "40d0fbd3-38a3-4a6e-8fe9-cfc56406749d",
          "jolocomWallet": {
              "id": 1,
              "encryptedSeedHex": "f82494567241333cadb3be24e8735f04fede1293109a2007e18b5381fc83f1733e899107c95c14bf6c7c0257d2a74a457e78d45570a333a9feffad1ba0faceef",
              "password": "7c4c3e94eb97fa4fab723bc4c2206704"
          }
      },
      "jolocomType": {
          "id": 1,
          "type": "FirstNameCredential",
          "name": "First Name Credential",
          "context": [
              {
                  "lastName": "https://schema.org/givenName"
              }
          ],
          "claimInterface": {
              "lastName": ""
          }
      },
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
          "jolocomCredentialTypeId must be a number conforming to the specified constraints"
      ],
      "error": "Bad Request"
    }
    ```
  - ### Code
    500 Internal Server Error
    ### Content
    ```json
    {
      "statusCode": 500,
      "message": "Internal server error"
    }
    ```