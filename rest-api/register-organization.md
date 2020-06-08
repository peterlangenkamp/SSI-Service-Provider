# Register Organization
Register a new organization that will be able to issue or verify credentials using the ssi service. NOTE: this can take a moment to complete as it also creates, fuels and registers the required Jolocom wallet.

- ## Url
  `/api/organizations/`

- ## Method
  `POST`

- ## URL Params
  None

- ## Body Params
  *JSON object with the following params:*
  ### Required
  `name=[string]`
  
  ### Example
  ```json
  {
      "name": "New Org"
  }
  ```

- ## Success Response
  - ### Code
    201 Created
    ### Content
    ```json
    {
        "name": "New org",
        "sharedSecret": "76cd77019a62b7c1b0a665bdfec941debbff7c5360f65541016e04db12cbdac8",
        "id": 1,
        "uuid": "40d0fbd3-38a3-4a6e-8fe9-cfc56406749d"
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
            "name should not be empty",
            "name must be a string"
        ],
        "error": "Bad Request"
    }
    ```