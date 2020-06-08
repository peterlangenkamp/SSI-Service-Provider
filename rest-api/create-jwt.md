# Create jwt
API to generate a JSON Web Token (JWT).

- ## Url
  `/api/utils/jwt/:organizationId`

- ## Method
  `POST`

- ## URL Params
  ### Required
  `organizationId=[string]`

- ## Body Params
  *JSON object*
  
  ### Example:
  ```json
  {
    "type": "FirstNameCredential",
    "callbackUrl": "https://jwt.io/"
  }
  ```

- ## Success Response
  - ### Code
    201 Created
    ### Content
    ```
    eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0eXBlIjoiRmlyc3ROYW1lQ3JlZGVudGlhbCIsImNhbGxiYWNrVXJsIjoiaHR0cHM6Ly9qd3QuaW8vIiwiaWF0IjoxNTkwODI0ODc2LCJhdWQiOiJzc2ktc2VydmljZS1wcm92aWRlciIsImlzcyI6IjQwZDBmYmQzLTM4YTMtNGE2ZS04ZmU5LWNmYzU2NDA2NzQ5ZCIsImp0aSI6IkR2ekdKRW9FdWhwaSJ9.mjCqkRpXzdr4EXpEVSeMxNzSjFbt641qhIOWJ7y2YJ4
    ```
    - ### Decoded JWT
      ```json
      {
        "type": "FirstNameCredential",
        "callbackUrl": "https://jwt.io/",
        "iat": 1590824876,
        "aud": "ssi-service-provider",
        "iss": "40d0fbd3-38a3-4a6e-8fe9-cfc56406749d",
        "jti": "DvzGJEoEuhpi"
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