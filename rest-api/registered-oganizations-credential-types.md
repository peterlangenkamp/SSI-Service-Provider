# Registered Organization's Credential Types
Retrieve a list of all credential type mappings (for all organizations).

- ## Url
  `/api/types`

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
          "type": "LastNameCredential",
          "irmaType": null,
          "jolocomType": {
              "id": 2,
              "type": "LastNameCredential",
              "name": "Last Name Credential",
              "context": [
                  {
                      "lastName": "https://schema.org/givenName"
                  }
              ],
              "claimInterface": {
                  "lastName": ""
              }
          },
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
          }
      },
      {
          "id": 2,
          "type": "FirstNameCredential",
          "irmaType": "irma-demo.MijnOverheid.fullName",
          "jolocomType": {
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
          }
      },
      {
          "id": 3,
          "type": "FirstNameCredential",
          "irmaType": "irma-demo.MijnOverheid.fullName",
          "jolocomType": {
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
          "organization": {
              "id": 2,
              "name": "My org",
              "sharedSecret": "7f4ff0007fc85ae20dafa9bb7f07a141feaf36f9ffdcf96d60dafa5656a7d87a",
              "uuid": "cd213adb-95f9-461e-9edf-5b6113748177",
              "jolocomWallet": {
                  "id": 2,
                  "encryptedSeedHex": "4590fe7181ffa688c3108dfa8152df5f18438fe8c4a07c500c2128d2d7f60c9b70136f531c7c3e43a6a5104b233fed4d6bb9ffaa61cd98b8c063b4987b678e22",
                  "password": "5a6b80bfa46206a14e64135e8776736f"
              }
          }
      },
      {
          "id": 4,
          "type": "LastNameCredential",
          "irmaType": null,
          "jolocomType": {
              "id": 2,
              "type": "LastNameCredential",
              "name": "Last Name Credential",
              "context": [
                  {
                      "lastName": "https://schema.org/givenName"
                  }
              ],
              "claimInterface": {
                  "lastName": ""
              }
          },
          "organization": {
              "id": 2,
              "name": "My org",
              "sharedSecret": "7f4ff0007fc85ae20dafa9bb7f07a141feaf36f9ffdcf96d60dafa5656a7d87a",
              "uuid": "cd213adb-95f9-461e-9edf-5b6113748177",
              "jolocomWallet": {
                  "id": 2,
                  "encryptedSeedHex": "4590fe7181ffa688c3108dfa8152df5f18438fe8c4a07c500c2128d2d7f60c9b70136f531c7c3e43a6a5104b233fed4d6bb9ffaa61cd98b8c063b4987b678e22",
                  "password": "5a6b80bfa46206a14e64135e8776736f"
              }
          }
      }
    ]
    ```

- ## Error Response
  \-