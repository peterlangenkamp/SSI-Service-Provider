# Credential Verify Request
API to execute a credential issue request (i.e. use the service to offer a credential to a user).

- ## Url
  `/api/issue`

- ## Method
  `GET`

- ## URL Params
  None

- ## Query Params
  ### Required
  - `token=[string]`

    This should be a jwt, as described [here](../jwt-descriptions/jwt-credential-verify-request.md).

- ## Body Params
  None

- ## Success Response
  - ### Code
    200 OK
    ### Content
    ```json
    {
      "verifyRequest": {
        "id": 5,
        "callbackUrl": "http://httpbin.org/get?response=",
        "uuid": "28e1fde2-e83e-44cb-9bb1-d17a6643be52",
        "jwtId": "fKFqBLnWgo8b",
        "hash": "acadcc285cf49b1cbc7585e4dc70f4950f221255ee880a5a9fb6b34f13b91b63",
        "type": {
          "id": 1,
          "type": "FirstNameCredential",
          "irmaType": "irma-demo.MijnOverheid.fullName",
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
          }
        },
        "requestor": {
          "id": 1,
          "name": "New org",
          "sharedSecret": "76cd77019a62b7c1b0a665bdfec941debbff7c5360f65541016e04db12cbdac8",
          "uuid": "40d0fbd3-38a3-4a6e-8fe9-cfc56406749d",
          "jolocomWallet": {
            "id": 1,
            "encryptedSeedHex": "f82494567241333cadb3be24e8735f04fede1293109a2007e18b5381fc83f1733e899107c95c14bf6c7c0257d2a74a457e78d45570a333a9feffad1ba0faceef",
            "password": "7c4c3e94eb97fa4fab723bc4c2206704"
          }
        }
      },
      "availableConnectors": [
        "jolocom",
        "irma"
      ]
    }
    ```

- ## Error Response
  - ### Code
    500 Internal Server Error
    ### Content
    ```json
    {
      "statusCode": 500,
      "message": "Internal server error"
    }
    ```