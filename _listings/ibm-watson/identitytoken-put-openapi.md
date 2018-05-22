---
swagger: "2.0"
x-collection-name: IBM Watson
x-complete: 0
info:
  title: IBM Watson Machine Learning Put Entity Token
  description: Refreshes token, accepts expired token and generates a new one (if
    the application binding / service key is still valid)
  version: 1.0.0
host: ibm-watson-ml.mybluemix.net
basePath: v3/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /identity/token:
    get:
      summary: Get Entity Token
      description: Tokens are required for the ML REST API authentication. They are
        generated using ML service credentials
      operationId: generateToken
      x-api-path-slug: identitytoken-get
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Identity
      - Token
    put:
      summary: Put Entity Token
      description: Refreshes token, accepts expired token and generates a new one
        (if the application binding / service key is still valid)
      operationId: refreshes-token-accepts-expired-token-and-generates-a-new-one-if-the-application-binding--service-ke
      x-api-path-slug: identitytoken-put
      parameters:
      - in: body
        name: token
        description: existing token
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Identity
      - Token
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---