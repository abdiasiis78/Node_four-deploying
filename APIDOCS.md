#Introduction
##BOOKSTORE API Documentation
###Base URL 
The base URL for this API is: `https://node-four-deploying.onrender.com`


###Owner Sign-up and Login

##Sign-up Owner
Endpoint: `/api/owner/signup`
Method: POST

`Request`
```{
  "name": "ali Doli",
  "email": "Doli@example.com",
  "password": "securepassword"
}```

`name` (string, required): The name of the owner.
`email` (string, required): The email address of the owner.
`password` (string, required): The owner's password.


###Response (Success - 201 Created)

`{
  "message": "Owner creation successful",
  "owner": {
    "id": 1,
     "name": "ali Doli",
  "email": "Doli@example.com",
  }
}
`

Response (Error - 409 Conflict)
`{
  "message": "Owner already exists"
}
`

Response (Error - 500 Internal Server Error)
`{
  "message": "Something went wrong",
  "error": "Internal server error message"
}`
