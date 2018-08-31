{
  "info": {
    "name": "IBM Watson IoT Platform Query draft phyiscal interfaces",
    "_postman_id": "c32f740c-69fe-4788-9eaf-f0ba3986b28f",
    "description": "Physical interfaces are used to model the interfaces between physical\ndevices and the Watson IoT Platform.  A physical interface references\nevent types.  Devices that implement a physical interface publish these\nevents to the platform.\n\nThe event types are referenced via a mapping that maps an event id to\nthe id of an event type.  The event id corresponds to the MQTT topic\nthat the event is published to by a device.\n\nThe **/draft/physicalinterfaces** endpoint returns the list of all of \nthe draft physical interfaces that have been defined for the\norganization in the Watson IoT Platform.  Various query parameters can\nbe used to filter, sort and page through the list of draft physical\ninterfaces that are returned.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Internet of Things",
      "item": [
        {
          "id": "d9f5091c-933c-41c9-aeb4-9daae1ccd8ba",
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
              "id": "0d4d9ca2-730f-40f9-b1d5-a75fe728747e"
            }
          ]
        },
        {
          "id": "95e990da-f904-4a92-a8ee-10aa03ec6310",
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
              "id": "7ca1ddf5-9bd0-4d7f-9725-ce9e484c33be"
            }
          ]
        },
        {
          "id": "6f2e3ad0-0456-4814-901e-d3f810bee169",
          "name": "retrieve-the-list-of-event-mappings-for-the-active-physical-interfaceevent-mappings-are-keyed-off-of",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "v0002",
                "physicalinterfaces/:physicalInterfaceId/events"
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
            "description": "Retrieve the list of event mappings for the active physical interface.\nEvent mappings are keyed off of the event id specified in the MQTT topic\nthat the inbound events are published to."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8f403b49-a91b-4d8c-90bc-7944ec3c0956"
            }
          ]
        },
        {
          "id": "84292a7a-6caf-4139-bbea-d6fdaa331504",
          "name": "physical-interfaces-are-used-to-model-the-interfaces-between-physicaldevices-and-the-watson-iot-plat1",
          "request": {
            "url": "http://example.com/api/v0002/draft/physicalinterfaces?No Name=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Physical interfaces are used to model the interfaces between physical\ndevices and the Watson IoT Platform.  A physical interface references\nevent types.  Devices that implement a physical interface publish these\nevents to the platform.\n\nThe event types are referenced via a mapping that maps an event id to\nthe id of an event type.  The event id corresponds to the MQTT topic\nthat the event is published to by a device.\n\nThe **/draft/physicalinterfaces** endpoint returns the list of all of \nthe draft physical interfaces that have been defined for the\norganization in the Watson IoT Platform.  Various query parameters can\nbe used to filter, sort and page through the list of draft physical\ninterfaces that are returned."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f14c8404-f4c9-4d51-bf7c-a876fe258ee8"
            }
          ]
        }
      ]
    }
  ]
}