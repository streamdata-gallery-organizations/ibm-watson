{
  "info": {
    "name": "IBM Watson IoT Platform Query draft schema definitions",
    "_postman_id": "f5534d39-8266-472a-996d-5d3b7f5c3474",
    "description": "Schemas are used to define the structure of Events, Device State and\nThing State in the Watson IoT Platform.\n\n  - For Events, they define the structure of the payload of the events\n    that are published to the platform by devices.\n\n  - For Device and Thing State, they define the structure of the state\n    that is stored by the platform.\n\nThe **/draft/schemas** endpoint returns the list of all of the draft \nschema for the organization in the Watson IoT Platform.  Various query\nparameters can be used to filter, sort and page through the list of\nschemas that are returned.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Internet of Things",
      "item": [
        {
          "id": "caf16604-8cbc-4fd9-98b2-bd30f7e08cfd",
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
              "id": "e78edb7d-d770-4dbc-a0c9-53b4b9627492"
            }
          ]
        },
        {
          "id": "a58bb616-b29e-4ea5-a2da-33622b21a20f",
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
              "id": "3fdaad92-f794-4ab8-8930-9435a008862e"
            }
          ]
        },
        {
          "id": "1cbaf93c-0e1f-4250-aeda-ccba6bed76ee",
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
              "id": "3723bbbb-0978-4466-866b-cb36681a2bf4"
            }
          ]
        },
        {
          "id": "c8730223-1806-468d-bcea-78391ed6bd10",
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
              "id": "46425cde-fccf-4ee9-b5a0-b04728334946"
            }
          ]
        }
      ]
    }
  ]
}