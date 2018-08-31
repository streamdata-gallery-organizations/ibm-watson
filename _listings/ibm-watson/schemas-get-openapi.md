---
swagger: "2.0"
x-collection-name: IBM Watson
x-complete: 0
info:
  title: IBM Watson IoT Platform Query active schema definitions
  description: "Schemas are used to define the structure of Events, Device State and\nThing
    State in the Watson IoT Platform.\n\n  - For Events, they define the structure
    of the payload of the events\n    that are published to the platform by devices.\n\n
    \ - For Device and Thing State, they define the structure of the state\n    that
    is stored by the platform.\n\nThe **schemas** endpoint returns the list of all
    of the active schema \ndefinitions for the organization in the Watson IoT Platform.
    \ Various\nquery parameters can be used to filter, sort and page through the list\nof
    schemas that are returned."
  version: 1.0.0
basePath: /api/v0002
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /schemas:
    get:
      summary: Query active schema definitions
      description: "Schemas are used to define the structure of Events, Device State
        and\nThing State in the Watson IoT Platform.\n\n  - For Events, they define
        the structure of the payload of the events\n    that are published to the
        platform by devices.\n\n  - For Device and Thing State, they define the structure
        of the state\n    that is stored by the platform.\n\nThe **schemas** endpoint
        returns the list of all of the active schema \ndefinitions for the organization
        in the Watson IoT Platform.  Various\nquery parameters can be used to filter,
        sort and page through the list\nof schemas that are returned."
      operationId: schemas-are-used-to-define-the-structure-of-events-device-state-andthing-state-in-the-watson-iot-pla
      x-api-path-slug: schemas-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Schemas
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