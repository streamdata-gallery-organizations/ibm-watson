{
  "info": {
    "name": "IBM Watson IoT Platform Get the list of active property mappings for the device type",
    "_postman_id": "c1b2dc34-2396-432b-8f19-f7377020dae3",
    "description": "Retrieve the list of active property mappings for the specified device\ntype.  A property mapping defines how properties from inbound events are\nmapped to properties defined on an logical interface associated with\nthe device type.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Internet of Things",
      "item": [
        {
          "id": "8307219f-2ad5-47e2-9bd9-467ce596ddbe",
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
              "id": "49e11bfc-c82a-44de-a216-ec4a54cc732b"
            }
          ]
        }
      ]
    }
  ]
}