{
  "info": {
    "name": "IBM Watson IoT Platform Get active schema definition metadata",
    "_postman_id": "d3bc2641-f528-4ec3-a34f-5cac654dce13",
    "description": "Retrieves the metadata for the active schema definition with the\nspecified id.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Internet of Things",
      "item": [
        {
          "id": "ee6f00cc-6b24-4530-9944-8a2103a2b082",
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
              "id": "dfcd1224-449b-4472-b8c8-7315a730513a"
            }
          ]
        },
        {
          "id": "87317a70-8c66-43ec-8d8f-2a88812216d6",
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
              "id": "d1329cb7-7e73-49c3-aafe-430af2967ba1"
            }
          ]
        }
      ]
    }
  ]
}