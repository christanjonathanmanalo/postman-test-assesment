# Postman API Testing Assessment

This repository contains my Postman API testing implementation.

## Collection

`postman-test`

### Requests covered

1. POST `/token`
2. GET `/users`
3. GET `/users/{userId}`
4. POST `/users`
5. PUT `/users`
6. DELETE `/users/{userId}`

## Test coverage

The collection validates HTTP status codes, response structure/content, user IDs, and token generation.

The token request stores the returned access token in the Postman environment so authenticated requests can reuse it through `{{token}}`.

## Files

- `postman-test.postman_collection.json` — Postman collection
- `postman-test.postman_environment.json` — Postman environment

## Security

No real access token is stored in this repository. The environment token variable is intentionally blank and is populated dynamically by the `/token` request.

## How to run

1. Import the collection and environment into Postman.
2. Select the `postman-test` environment.
3. Run `POST /token` first to generate and store the token.
4. Run the remaining requests individually or through the Postman Collection Runner.
