# Flask-API OpenAPI (Swagger) — Converted

**Source:** `swagger/swagger.yml`

**Version:** 1.0.0

**Description:** This is the swagger spec for the flask API

**Consumes:** `application/json`

**Produces:** `application/json`

---

## Paths

### GET /
- OperationId: `api.main.welcome`
- Tags: `welcome`
- Summary: Retrieves welcome message
- Description: Displays welcome message
- Responses:
  - 200: See a welcome message

### GET /health
- OperationId: `api.main.health`
- Tags: `health`
- Summary: Retrieves health status of this application
- Description: Perform health check on Flask API
- Responses:
  - 200: Application is running normally

### GET /users/v1
- OperationId: `api.users.get_users`
- Tags: `users`
- Summary: Retrieves all users
- Description: Displays all users
- Responses:
  - 200: See all users

### GET /users/v1/{username}
- OperationId: `api.users.get_by_username`
- Tags: `users`
- Summary: Retrieves an individual user
- Description: Displays user by username

Parameters:
- `username` (path, required, string) — retrieve username data

Responses:
- 200: Successfully displays user info
  - Schema: array of objects
    - Item properties:
      - `username`: string
      - `email`: string
- 404: User not found

---

## Notes
- This Markdown is a direct, human-friendly rendering of the Swagger (OpenAPI 2.0) file located at `swagger/swagger.yml`.
- If you want an expanded rendering (detailed request/response examples, request body schemas, or a table of parameters), tell me which endpoints to expand and I will update the file.
