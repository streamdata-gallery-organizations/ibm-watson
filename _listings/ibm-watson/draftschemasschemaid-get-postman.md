{
  "info": {
    "name": "IBM Watson IoT Platform Get draft schema definition metadata",
    "_postman_id": "70c7c6d7-505f-452a-9297-8545396052e2",
    "description": "Retrieves the metadata for the draft schema definition with the\nspecified id.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Internet of Things",
      "item": [
        {
          "id": "1de818b6-0927-4e6f-911f-3f287d9b12d6",
          "name": "schemas-are-used-to-define-the-structure-of-events-device-state-andthing-state-in-the-watson-iot-pla",
          "request": {
            "url": "http://example.com/api/v0002/schemas?No Name=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Schemas are used to define the structure of Events, Device State and\nThing State in the Watson IoT Platform.\n\n  - For Events, they define the structure of the payload of the events\n    that are published to the platform by devices.\n\n  - For Device and Thing State, they define the structure of the state\n    that is stored by the platform.\n\nThe **schemas** endpoint returns the list of all of the active schema \ndefinitions for the organization in the Watson IoT Platform.  Various\nquery parameters can be used to filter, sort and page through the list\nof schemas that are returned."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f35e4d5b-ac95-437a-a8bf-97e1bee63164"
            }
          ]
        },
        {
          "id": "3ea0d7a2-567e-45c8-bcdf-3c9028e0ef2d",
          "name": "retrieves-the-metadata-for-the-active-schema-definition-with-thespecified-id",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "v0002",
                "schemas/:schemaId"
              ],
              "query": [
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "schemaId",
                  "value": "schemaId",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves the metadata for the active schema definition with the\nspecified id."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9ed2077d-c3e8-472d-92d2-eded82bce1eb"
            }
          ]
        },
        {
          "id": "8184f648-8089-4a52-9db0-291038ecc105",
          "name": "retrieves-the-content-of-the-active-schema-definition-file-with-thespecified-id",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "v0002",
                "schemas/:schemaId/content"
              ],
              "query": [
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "schemaId",
                  "value": "schemaId",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves the content of the active schema definition file with the\nspecified id."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d23b000f-b5e9-4341-95ef-3f777e4ee98a"
            }
          ]
        },
        {
          "id": "e42849c7-c718-4fa1-baeb-ddc4e28bf4a4",
          "name": "schemas-are-used-to-define-the-structure-of-events-device-state-andthing-state-in-the-watson-iot-pla1",
          "request": {
            "url": "http://example.com/api/v0002/draft/schemas?No Name=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Schemas are used to define the structure of Events, Device State and\nThing State in the Watson IoT Platform.\n\n  - For Events, they define the structure of the payload of the events\n    that are published to the platform by devices.\n\n  - For Device and Thing State, they define the structure of the state\n    that is stored by the platform.\n\nThe **/draft/schemas** endpoint returns the list of all of the draft \nschema for the organization in the Watson IoT Platform.  Various query\nparameters can be used to filter, sort and page through the list of\nschemas that are returned."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "18d1378f-8db2-48ea-ae72-9fad92971a41"
            }
          ]
        },
        {
          "id": "6ff6e8cb-7bde-4707-b5ad-ad030a98524c",
          "name": "creates-a-new-draft-schema-definition-for-the-organization-in-the-watsoniot-platformthe-schema-defin",
          "request": {
            "url": "http://example.com/api/v0002/draft/schemas?No Name=%7B%7D",
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a new draft schema definition for the organization in the Watson\nIoT Platform.\n\nThe schema definition file is passed to the Watson IoT Platform within a\nmultipart POST (multipart/form-data).  The body of the POST **must**\ncontain at least two parts:\n\n  - One with a name of **schemaFile** that contains the actual content\n    of the file as the body of the part.\n    \n  - One with a name of **name** that contains a string that defines the\n    name of the schema resource in the body of the part.\n\nAdditional metadata can be passed in other parts within the multipart\nPOST.  For example, to specify a description for the new schema\ndefinition, you should include a part with the name **description** and\nthe description as the body of the part.  To specify the type of the\nschema, you should include a part with the name **schemaType** and one\nof the following in the body of the part (the schemaType defaults to\njson-schema if the no schemaType part is present):\n\n  - json-schema\n\nIf parts with names other than those specified above are included in the\nmultipart POST the request will fail and an HTTP status code of 400 will\nbe returned.\n\nThe content of the schema definition file that is passed to the platform\nis stored and a REST resource is created containing metadata that\ndescribes the schema definition."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b2b1e5b3-23a2-4aab-832e-df32029cc69f"
            }
          ]
        },
        {
          "id": "e38a2be7-464c-4eb4-b03f-208c37d7b85b",
          "name": "retrieves-the-metadata-for-the-draft-schema-definition-with-thespecified-id",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "v0002",
                "draft/schemas/:schemaId"
              ],
              "query": [
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "schemaId",
                  "value": "schemaId",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves the metadata for the draft schema definition with the\nspecified id."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "276fc43a-8819-48ae-9557-a1b9436d2fe2"
            }
          ]
        }
      ]
    }
  ]
}