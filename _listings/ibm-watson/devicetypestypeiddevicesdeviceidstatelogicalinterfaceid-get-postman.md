{
  "info": {
    "name": "IBM Watson IoT Platform Get the state for the device with the specified id",
    "_postman_id": "449d625e-d18a-44e1-b30a-83671bebdbe8",
    "description": "Retrieve the current state of the device with the specified id.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Internet of Things",
      "item": [
        {
          "id": "28af1b74-cfc2-4627-b524-073d8fafb268",
          "name": "retrieve-the-current-state-of-the-device-with-the-specified-id",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "v0002",
                "device/types/:typeId/devices/:deviceId/state/:logicalInterfaceId"
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
                  "id": "typeId",
                  "value": "typeId",
                  "type": "string"
                },
                {
                  "id": "deviceId",
                  "value": "deviceId",
                  "type": "string"
                },
                {
                  "id": "logicalInterfaceId",
                  "value": "logicalInterfaceId",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve the current state of the device with the specified id."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5ce7480d-78f7-403e-9dd3-95c250fbda19"
            }
          ]
        }
      ]
    }
  ]
}