{
  "info": {
    "name": "IBM Watson IoT Platform Get the contents of the active schema definition file",
    "_postman_id": "a1b9dcb1-ef65-48ea-8023-93a1623dff07",
    "description": "Retrieves the content of the active schema definition file with the\nspecified id.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Internet of Things",
      "item": [
        {
          "id": "7f27839e-2163-4513-9288-0c9c4949c313",
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
              "id": "7609ee39-a561-48fd-a306-1c41cf42619f"
            }
          ]
        },
        {
          "id": "1111a506-f0d6-4ee4-97b4-58a55d5972ce",
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
              "id": "5be92d00-8b6c-453f-ae39-08a74c019d5c"
            }
          ]
        },
        {
          "id": "ab49815d-9fbd-48cf-abbd-fa7a4212d73e",
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
              "id": "fbbc367b-a1dd-4473-adf7-8f5e7a013797"
            }
          ]
        }
      ]
    }
  ]
}