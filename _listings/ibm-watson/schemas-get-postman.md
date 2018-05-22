{
  "info": {
    "name": "IBM Watson IoT Platform Query active schema definitions",
    "_postman_id": "1701af38-081c-4057-a583-ea7f8457c437",
    "description": "Schemas are used to define the structure of Events, Device State and\nThing State in the Watson IoT Platform.\n\n  - For Events, they define the structure of the payload of the events\n    that are published to the platform by devices.\n\n  - For Device and Thing State, they define the structure of the state\n    that is stored by the platform.\n\nThe **schemas** endpoint returns the list of all of the active schema \ndefinitions for the organization in the Watson IoT Platform.  Various\nquery parameters can be used to filter, sort and page through the list\nof schemas that are returned.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Internet of Things",
      "item": [
        {
          "id": "d08ba6d1-de63-49f6-bd45-554b1caa6d58",
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
              "id": "413d5834-13e8-4f79-9496-8cf47d4e1089"
            }
          ]
        }
      ]
    }
  ]
}