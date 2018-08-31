{
  "info": {
    "name": "IBM Watson IoT Platform Get an active physical interface",
    "_postman_id": "29db09fd-b616-4da9-a5ac-3a4db7ac795c",
    "description": "Retrieve the active physical interface with the specified id.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Internet of Things",
      "item": [
        {
          "id": "b3c9b967-1569-4454-a71e-d2e4a9013f22",
          "name": "physical-interfaces-are-used-to-model-the-interfaces-between-physicaldevices-and-the-watson-iot-plat",
          "request": {
            "url": "http://example.com/api/v0002/physicalinterfaces?No Name=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Physical interfaces are used to model the interfaces between physical\ndevices and the Watson IoT Platform.  A physical interface references\nevent types.  Devices that implement a physical interface publish these\nevents to the platform.\n\nThe event types are referenced via a mapping that maps an event id to\nthe id of an event type.  The event id corresponds to the MQTT topic\nthat the event is published to by a device.\n\nThe **physicalinterfaces** endpoint returns the list of all of the\nactive physical interfaces that have been defined for the organization\nin the Watson IoT Platform.  Various query parameters can be used to\nfilter, sort and page through the list of active physical interfaces\nthat are returned."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "31f265e2-0b8b-4ca3-949f-91c5e7e8a65b"
            }
          ]
        },
        {
          "id": "ea7883e7-42f4-40e4-882e-f3641020e5d4",
          "name": "retrieve-the-active-physical-interface-with-the-specified-id",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "v0002",
                "physicalinterfaces/:physicalInterfaceId"
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
                  "id": "physicalInterfaceId",
                  "value": "physicalInterfaceId",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve the active physical interface with the specified id."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d258f3f4-ac3e-4531-9a8c-db9a75a24d39"
            }
          ]
        }
      ]
    }
  ]
}