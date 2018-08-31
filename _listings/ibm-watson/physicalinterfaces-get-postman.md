{
  "info": {
    "name": "IBM Watson IoT Platform Query active phyiscal interfaces",
    "_postman_id": "bec7fd5d-59f2-4ed3-89cf-902f57c39c49",
    "description": "Physical interfaces are used to model the interfaces between physical\ndevices and the Watson IoT Platform.  A physical interface references\nevent types.  Devices that implement a physical interface publish these\nevents to the platform.\n\nThe event types are referenced via a mapping that maps an event id to\nthe id of an event type.  The event id corresponds to the MQTT topic\nthat the event is published to by a device.\n\nThe **physicalinterfaces** endpoint returns the list of all of the\nactive physical interfaces that have been defined for the organization\nin the Watson IoT Platform.  Various query parameters can be used to\nfilter, sort and page through the list of active physical interfaces\nthat are returned.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Internet of Things",
      "item": [
        {
          "id": "045b3eeb-fca5-4c30-98f6-db864bbf19e6",
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
              "id": "a31b4e77-c50a-4e80-abac-e4db3d085f96"
            }
          ]
        }
      ]
    }
  ]
}