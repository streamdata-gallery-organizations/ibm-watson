{
  "info": {
    "name": "IBM Watson IoT Platform Get the list of event mappings",
    "_postman_id": "0554bc85-c24d-4f26-a64c-610c272597fa",
    "description": "Retrieve the list of event mappings for the active physical interface.\nEvent mappings are keyed off of the event id specified in the MQTT topic\nthat the inbound events are published to.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Internet of Things",
      "item": [
        {
          "id": "7b67d7b0-c829-4343-bfe6-95b5b1ffe0a5",
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
              "id": "aec96dd2-c063-4884-9e62-48e579aa0c85"
            }
          ]
        },
        {
          "id": "c6e21b15-f34c-4ad9-9de3-e42d2e157472",
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
              "id": "f6c6d5f5-efbb-4a27-8ed3-3ac9326b2a21"
            }
          ]
        },
        {
          "id": "18432e9d-22ae-4f40-938e-0c83ea1d8bd6",
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
              "id": "55f3e0ea-7a30-4749-85eb-f41888b6c93f"
            }
          ]
        }
      ]
    }
  ]
}