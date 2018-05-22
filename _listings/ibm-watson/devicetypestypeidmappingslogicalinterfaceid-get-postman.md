{
  "info": {
    "name": "IBM Watson IoT Platform Get the active property mappings for a specific logical interface\nfor a device type.",
    "_postman_id": "3b06daa4-a8c5-499f-97d0-b235793f1b9a",
    "description": "Retrieves the active property mappings for a specific logical\ninterface for the device type.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Internet of Things",
      "item": [
        {
          "id": "d257651f-c2a6-46d0-8ffd-0a064aad7baa",
          "name": "retrieve-the-list-of-active-property-mappings-for-the-specified-devicetype--a-property-mapping-defin",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "v0002",
                "device/types/:typeId/mappings"
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
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve the list of active property mappings for the specified device\ntype.  A property mapping defines how properties from inbound events are\nmapped to properties defined on an logical interface associated with\nthe device type."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0c056768-f2f1-4c00-a08c-6a08bc981bd1"
            }
          ]
        },
        {
          "id": "1c440c1f-f8e7-4aca-b0f3-0f91f6721ff6",
          "name": "retrieves-the-active-property-mappings-for-a-specific-logicalinterface-for-the-device-type",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "v0002",
                "device/types/:typeId/mappings/:logicalInterfaceId"
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
            "description": "Retrieves the active property mappings for a specific logical\ninterface for the device type."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7f27006e-a7b6-4945-b3cd-07d84dea065f"
            }
          ]
        }
      ]
    }
  ]
}