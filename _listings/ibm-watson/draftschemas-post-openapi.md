---
swagger: "2.0"
x-collection-name: IBM Watson
x-complete: 0
info:
  title: IBM Watson IoT Platform Create a draft schema definition
  description: "Creates a new draft schema definition for the organization in the
    Watson\nIoT Platform.\n\nThe schema definition file is passed to the Watson IoT
    Platform within a\nmultipart POST (multipart/form-data).  The body of the POST
    **must**\ncontain at least two parts:\n\n  - One with a name of **schemaFile**
    that contains the actual content\n    of the file as the body of the part.\n    \n
    \ - One with a name of **name** that contains a string that defines the\n    name
    of the schema resource in the body of the part.\n\nAdditional metadata can be
    passed in other parts within the multipart\nPOST.  For example, to specify a description
    for the new schema\ndefinition, you should include a part with the name **description**
    and\nthe description as the body of the part.  To specify the type of the\nschema,
    you should include a part with the name **schemaType** and one\nof the following
    in the body of the part (the schemaType defaults to\njson-schema if the no schemaType
    part is present):\n\n  - json-schema\n\nIf parts with names other than those specified
    above are included in the\nmultipart POST the request will fail and an HTTP status
    code of 400 will\nbe returned.\n\nThe content of the schema definition file that
    is passed to the platform\nis stored and a REST resource is created containing
    metadata that\ndescribes the schema definition."
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
  /schemas/{schemaId}:
    get:
      summary: Get active schema definition metadata
      description: |-
        Retrieves the metadata for the active schema definition with the
        specified id.
      operationId: retrieves-the-metadata-for-the-active-schema-definition-with-thespecified-id
      x-api-path-slug: schemasschemaid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Schemas
      - SchemaId
  /schemas/{schemaId}/content:
    get:
      summary: Get the contents of the active schema definition file
      description: |-
        Retrieves the content of the active schema definition file with the
        specified id.
      operationId: retrieves-the-content-of-the-active-schema-definition-file-with-thespecified-id
      x-api-path-slug: schemasschemaidcontent-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Schemas
      - SchemaId
      - Content
  /draft/schemas:
    get:
      summary: Query draft schema definitions
      description: "Schemas are used to define the structure of Events, Device State
        and\nThing State in the Watson IoT Platform.\n\n  - For Events, they define
        the structure of the payload of the events\n    that are published to the
        platform by devices.\n\n  - For Device and Thing State, they define the structure
        of the state\n    that is stored by the platform.\n\nThe **/draft/schemas**
        endpoint returns the list of all of the draft \nschema for the organization
        in the Watson IoT Platform.  Various query\nparameters can be used to filter,
        sort and page through the list of\nschemas that are returned."
      operationId: schemas-are-used-to-define-the-structure-of-events-device-state-andthing-state-in-the-watson-iot-pla
      x-api-path-slug: draftschemas-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Schemas
    post:
      summary: Create a draft schema definition
      description: "Creates a new draft schema definition for the organization in
        the Watson\nIoT Platform.\n\nThe schema definition file is passed to the Watson
        IoT Platform within a\nmultipart POST (multipart/form-data).  The body of
        the POST **must**\ncontain at least two parts:\n\n  - One with a name of **schemaFile**
        that contains the actual content\n    of the file as the body of the part.\n
        \   \n  - One with a name of **name** that contains a string that defines
        the\n    name of the schema resource in the body of the part.\n\nAdditional
        metadata can be passed in other parts within the multipart\nPOST.  For example,
        to specify a description for the new schema\ndefinition, you should include
        a part with the name **description** and\nthe description as the body of the
        part.  To specify the type of the\nschema, you should include a part with
        the name **schemaType** and one\nof the following in the body of the part
        (the schemaType defaults to\njson-schema if the no schemaType part is present):\n\n
        \ - json-schema\n\nIf parts with names other than those specified above are
        included in the\nmultipart POST the request will fail and an HTTP status code
        of 400 will\nbe returned.\n\nThe content of the schema definition file that
        is passed to the platform\nis stored and a REST resource is created containing
        metadata that\ndescribes the schema definition."
      operationId: creates-a-new-draft-schema-definition-for-the-organization-in-the-watsoniot-platformthe-schema-defin
      x-api-path-slug: draftschemas-post
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
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