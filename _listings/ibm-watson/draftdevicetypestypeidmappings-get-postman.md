{
  "info": {
    "name": "IBM Watson IoT Platform Get the list of draft property mappings for the device type",
    "_postman_id": "c8fe041e-1ad4-4b67-9df8-11c566dbbf70",
    "description": "Retrieve the list of draft property mappings for the specified device\ntype.  A property mapping defines how properties from inbound events are\nmapped to properties defined on an logical interface associated with\nthe device type.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Internet of Things",
      "item": [
        {
          "id": "ecc96af8-33f6-4774-aac7-fe36e47f8247",
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
              "id": "86f1f091-8a5c-482f-85dd-97f664cc8afa"
            }
          ]
        },
        {
          "id": "53fd7a48-103b-4cba-afe1-522ce84955c4",
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
              "id": "a8a5ff77-270c-4808-9ecf-7a9443b5c8dd"
            }
          ]
        },
        {
          "id": "9609c9e0-5494-47d4-b574-94a6373ca008",
          "name": "retrieve-the-list-of-draft-property-mappings-for-the-specified-devicetype--a-property-mapping-define",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "v0002",
                "draft/device/types/:typeId/mappings"
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
            "description": "Retrieve the list of draft property mappings for the specified device\ntype.  A property mapping defines how properties from inbound events are\nmapped to properties defined on an logical interface associated with\nthe device type."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "07770707-4a13-4101-a0b9-eec2aab2148d"
            }
          ]
        }
      ]
    }
  ]
}