```yaml
swagger: "2.0"
info:
  description: This is the swagger spec for the flask API
  version: "1.0.0"
  title: Flask-API
consumes:
  - application/json
produces:
  - application/json


paths:
  /:
    get:
      operationId: api.main.welcome
      tags:
        - welcome
      summary: Retrieves welcome message
      description: Displays welcome message
      responses:
        200:
          description: See a welcome message

  /health:
    get:
      operationId: api.main.health
      tags:
        - health
      summary: Retrieves health status of this application
      description: Perform health check on Flask API
      responses:
        200:
          description: Application is running normally

  /users/v1:
    get:
      operationId: api.users.get_users
      tags:
        - users
      summary: Retrieves all users
      description: Displays all users
      responses:
        200:
          description: See all users

  /users/v1/{username}:
    get:
      operationId: api.users.get_by_username
      tags:
        - users
      summary: Retrieves an individual user
      description: Displays user by username
      parameters:
        - name: username
          in: path
          description: retrieve username data
          type: string
          required: true
      responses:
        200:
          description: Successfully displays user info
          schema:
            type: array
            items:
              properties:
                username:
                  type: string
                email:
                  type: string
        404:
          description: User not found
```