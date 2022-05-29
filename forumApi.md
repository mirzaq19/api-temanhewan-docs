# Temanhewan API Documentation

## API for FORUM

### Api untuk menambah forum
- URL: `/api/forum/create`
- Header: `Bearer <token>`
- Request Body:
  - `title`: `string`
  - `subtitle`: `string`
  - `content`: `string`
  - `forum_images[](optional)`: `file`
- Response:
  ```json
  {
    "success": true,
    "message": "success",
  }
  ```

### Api untuk get my list forum
- URL: `/api/forum/my`
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
              "id": "d41cb8e6-b588-41d8-93b1-d2df602dbe15",
              "slug": "how-can-i-generate-a-ad-preview-without-requiring-the-ad-account-id-in-the-facebook-ads-api",
              "title": "How can I generate a ad preview without requiring the ad account id in the Facebook Ads API?",
              "subtitle": "generate a ad preview without requiring the ad account id in the Facebook Ads API?",
              "content": "Though it is mentioned in the docs about generating a preview without requiring the ad_account_id (https://developers.facebook.com/docs/marketing-api/generatepreview/v13.0)."
              "forum_images": [
                  "http://api.temanhewan.local/storage/user/forum_images/165348843173.png",
                  "http://api.temanhewan.local/storage/user/forum_images/165348843157.png",
                  "http://api.temanhewan.local/storage/user/forum_images/165348843128.png",
                  "http://api.temanhewan.local/storage/user/forum_images/16534884314.png",
                  "http://api.temanhewan.local/storage/user/forum_images/165348843189.png"
              ],
              "created_at": "2022-05-25 21:20:31",
              "updated_at": "2022-05-25 21:20:31"
          },
          {
              "id": "07e1f858-67e8-4551-a61a-9f4f1eeaa2b1",
              "slug": "how-to-create-api-login-in-laravel-with-sanctum-autentication",
              "title": "How to create api login in laravel with sanctum autentication",
              "subtitle": "create api login with sanctum authentication",
              "content": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam convallis vitae felis eu pharetra. Vestibulum porta nunc tortor, ut lacinia maur."
              "forum_images": [
                  "http://api.temanhewan.local/storage/user/forum_images/165348828494.png",
                  "http://api.temanhewan.local/storage/user/forum_images/165348828442.png",
                  "http://api.temanhewan.local/storage/user/forum_images/165348828429.png"
              ],
              "created_at": "2022-05-25 21:18:04",
              "updated_at": "2022-05-25 21:18:04"
          }
      ]
  }
  ```
  
### Api untuk get forum 
- URL: `/api/forum/get`
- Header: `Bearer <token>`
- Request Body:
  - `id`: `string`
- Response:
  ```json
  {
      "success": true,
      "message": "success",
      "data": {
          "id": "07e1f858-67e8-4551-a61a-9f4f1eeaa2b1",
          "slug": "how-to-create-api-login-in-laravel-with-sanctum-autentication",
          "title": "How to create api login in laravel with sanctum autentication",
          "subtitle": "create api login with sanctum authentication",
          "content": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam convallis vitae felis eu pharetra."
          "forum_images": [
              "http://api.temanhewan.local/storage/user/forum_images/165348828494.png",
              "http://api.temanhewan.local/storage/user/forum_images/165348828442.png",
              "http://api.temanhewan.local/storage/user/forum_images/165348828429.png"
          ],
          "created_at": "2022-05-25 21:18:04",
          "updated_at": "2022-05-25 21:18:04"
      }
  }
  ```
