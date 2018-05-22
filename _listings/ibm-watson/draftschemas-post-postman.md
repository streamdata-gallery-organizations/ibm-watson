{
  "info": {
    "name": "IBM Watson IoT Platform Create a draft schema definition",
    "_postman_id": "8aaaab04-537c-40fa-a1c7-658f9aedd0c4",
    "description": "Creates a new draft schema definition for the organization in the Watson\nIoT Platform.\n\nThe schema definition file is passed to the Watson IoT Platform within a\nmultipart POST (multipart/form-data).  The body of the POST **must**\ncontain at least two parts:\n\n  - One with a name of **schemaFile** that contains the actual content\n    of the file as the body of the part.\n    \n  - One with a name of **name** that contains a string that defines the\n    name of the schema resource in the body of the part.\n\nAdditional metadata can be passed in other parts within the multipart\nPOST.  For example, to specify a description for the new schema\ndefinition, you should include a part with the name **description** and\nthe description as the body of the part.  To specify the type of the\nschema, you should include a part with the name **schemaType** and one\nof the following in the body of the part (the schemaType defaults to\njson-schema if the no schemaType part is present):\n\n  - json-schema\n\nIf parts with names other than those specified above are included in the\nmultipart POST the request will fail and an HTTP status code of 400 will\nbe returned.\n\nThe content of the schema definition file that is passed to the platform\nis stored and a REST resource is created containing metadata that\ndescribes the schema definition.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Internet of Things",
      "item": [
        {
          "id": "3542de3c-cd92-4312-b0b9-080a8681a88a",
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
              "id": "125a7e60-0886-46b0-9cdb-becc32e1cdae"
            }
          ]
        },
        {
          "id": "6cfd2e64-d676-416b-bff1-6a1d11773566",
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
              "id": "26680966-87c8-40cb-bb84-0323d8c2d88d"
            }
          ]
        },
        {
          "id": "f630102a-4699-4808-ba3d-7dff6b511af3",
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
              "id": "128fbd35-4e9a-44a0-959a-cd8f000554ca"
            }
          ]
        },
        {
          "id": "9e099273-7da6-4917-992a-5e7d8aaffa32",
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
              "id": "36695ff2-6f25-4762-8458-c4cf7f3fcefb"
            }
          ]
        },
        {
          "id": "c936909f-3e59-4e17-ba92-5f147ca997a8",
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
              "id": "971fb137-f2d0-469f-ae59-f945cbeaa212"
            }
          ]
        }
      ]
    }
  ]
}