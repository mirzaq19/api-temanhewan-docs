# Temanhewan API Documentation

## API for PET

### Api untuk menambah pet
- URL: `/api/pet/create`
- Header: `Bearer <token>`
- Request Body:
  - `name`: `string`
  - `profile_image(optional)`: `file`
  - `description(optional)`: `string`
  - `race`: `string('cat|'dog'')`
  - `gender`: `string( "m" | "f")`
- Response:
  ```json
  {
    "success": true,
    "message": "Pet Added Successfully",
    "data": {
        "id": "bdff2032-2865-4952-89ea-add7a4695663",
        "name": "bambang",
        "description": "kucing oren songong",
        "gender": "m",
        "race": "cat",
        "profile_image": "http://api.temanhewan.local/image/pet_default.png"
    }
  }
  ```

### Api untuk get my pet
- URL: `/api/pet/get`
- Header: `Bearer <token>`
- Request Body:
  - `id`: `string`
- Response:
  ```json
  {
    "success": true,
    "message": "Pet Added Successfully",
    "data": {
        "id": "bdff2032-2865-4952-89ea-add7a4695663",
        "name": "bambang",
        "description": "kucing oren songong",
        "gender": "m",
        "race": "cat",
        "profile_image": "http://api.temanhewan.local/image/pet_default.png"
    }
  }
  ```
  
### Api untuk list my pet 
- URL: `/api/pet/list`
- Header: `Bearer <token>`
- Request Body:
  - `offset`: `int`
  - `limit`: `int`
- Response:
  ```json
  {
      "success": true,
      "message": "success",
      "data": [
          {
              "id": "73f6765b-77bc-4038-8158-6e663f89670c",
              "name": "sam",
              "description": "anjing putih lucu",
              "gender": "m",
              "race": "dog",
              "profile_image": "http://api.temanhewan.local/image/pet_default.png"
          },
          {
              "id": "bdff2032-2865-4952-89ea-add7a4695663",
              "name": "bambang",
              "description": "kucing oren songong",
              "gender": "m",
              "race": "cat",
              "profile_image": "http://api.temanhewan.local/image/pet_default.png"
          }
      ]
  }
  ```
  
### Api untuk update pet 
- URL: `/api/pet/update`
- Header: `Bearer <token>`
- Request Body:
  - `id`: `string`
  - `name`: `string`
  - `profile_image(optional)`: `file`
  - `description(optional)`: `string`
  - `race`: `string('cat|'dog'')`
  - `gender`: `string( "m" | "f")`
- Response:
  ```json
  {
    "success": true,
    "message": "Pet Added Successfully",
    "data": {
        "id": "bdff2032-2865-4952-89ea-add7a4695663",
        "name": "bambang",
        "description": "kucing oren songong",
        "gender": "m",
        "race": "cat",
        "profile_image": "http://api.temanhewan.local/image/pet_default.png"
    }
  }
  ```
  
### Api untuk remove pet
- URL: `/api/pet/delete`
- Header: `Bearer <token>`
- Request Body:
  - `id`: `string`
- Response:
  ```json
  {
    "success": true
    "message": "Pet successfully deleted"
  }
  ```
