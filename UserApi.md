# Temanhewan API Documentation

## API for USER

### Api untuk register user 
- URL: `/api/user/register`
- Request Body:
  - `name`: `string`
  - `profile_image(optional)`: `file`
  - `birthdate`: `string`
  - `username`: `string`
  - `gender`: `string( "m" | "f")`
  - `role`: `string( "customer" | "doctor" | "grooming" )`
  - `email`: `string`
  - `password`: `string`
  - `password_confirmation`: `string`
  - `address`: `string`
  - `phone`: `string`
- Response:
  ```json
  {
    "success": true
    "message": "User created successfully"
  }
  ```

### Api untuk login user 
- URL: `/api/user/login`
- Request Body:
  - `email`: `string`
  - `password`: `string`
- Response:
  ```json
  {
    "success": true, 
    "message": "success", 
    "data": { 
       "user":{
          "id": "72c3473d-2701-4e19-8d44-5e4f757945da",
          "name": "M. Auliya Mirzaq Romdloni",
          "profile_image": "user_default.png"
          "birthdate": "2000-12-19",
          "username": "mirzaq19",
          "gender": "m",
          "role": "customer",
          "balance": 0,
          "email": "mirzaq@gmail.com",
          "email_verified_at": null,
          "address": "Japan raya, sooko, mojokerto",
          "phone": "082234260055",
          "created_at": "2022-05-22T01:10:51.000000Z",
          "updated_at": "2022-05-22T01:10:51.000000Z" 
          }, 
       "access_token": "<token>", 
       "token_type": "Bearer "
    }
  }
  ```
  
### Api untuk update user 
- URL: `/api/user/update`
- Header: `Bearer <token>`
- Request Body:
  - `name`: `string`
  - `profile_image(optional)`: `file`
  - `birthdate`: `string`
  - `gender`: `string( "m" | "f")`
  - `address`: `string`
  - `phone`: `string`
- Response:
  ```json
  {
    "success": true
    "message": "success"
  }
  ```
  
### Api untuk change password user 
- URL: `/api/user/change-password`
- Header: `Bearer <token>`
- Request Body:
  - `old_password`: `string`
  - `password`: `string`
  - `password_confirmation`: `string`
- Response:
  ```json
  {
    "success": true
    "message": "success"
  }
  ```
  
### Api untuk logout user 
- URL: `/api/user/logout`
- Header: `Bearer <token>`
- Response:
  ```json
  {
    "success": true
    "message": "success"
  }
  ```
