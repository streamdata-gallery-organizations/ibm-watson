---
name: IBM Watson
x-slug: ibm-watson
description: Meet IBM Watson, a cognitive system that enables a new partnership between
  people and computers that enhances and scales human expertise. Watson has been learning
  the language of professions and is trained by experts to work across many different
  industries.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
x-kinRank: "9"
x-alexaRank: "0"
tags: IBM Watson
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/apis.md
specificationVersion: "0.14"
apis:
- name: IBM Watson IoT Platform Query active schema definitions
  x-api-slug: ibm-watson-iot-platform
  description: "Schemas are used to define the structure of Events, Device State and\nThing
    State in the Watson IoT Platform.\n\n  - For Events, they define the structure
    of the payload of the events\n    that are published to the platform by devices.\n\n
    \ - For Device and Thing State, they define the structure of the state\n    that
    is stored by the platform.\n\nThe **schemas** endpoint returns the list of all
    of the active schema \ndefinitions for the organization in the Watson IoT Platform.
    \ Various\nquery parameters can be used to filter, sort and page through the list\nof
    schemas that are returned."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//schemas
  tags: Internet of Things,Schemas
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/schemas-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/schemas-get-openapi.md
- name: IBM Watson IoT Platform Get active schema definition metadata
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieves the metadata for the active schema definition with the
    specified id.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//schemas/{schemaId}
  tags: Internet of Things,Schemas,SchemaId
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/schemasschemaid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/schemasschemaid-get-openapi.md
- name: IBM Watson IoT Platform Get the contents of the active schema definition file
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieves the content of the active schema definition file with the
    specified id.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//schemas/{schemaId}/content
  tags: Internet of Things,Schemas,SchemaId,Content
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/schemasschemaidcontent-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/schemasschemaidcontent-get-openapi.md
- name: IBM Watson IoT Platform Query draft schema definitions
  x-api-slug: ibm-watson-iot-platform
  description: "Schemas are used to define the structure of Events, Device State and\nThing
    State in the Watson IoT Platform.\n\n  - For Events, they define the structure
    of the payload of the events\n    that are published to the platform by devices.\n\n
    \ - For Device and Thing State, they define the structure of the state\n    that
    is stored by the platform.\n\nThe **/draft/schemas** endpoint returns the list
    of all of the draft \nschema for the organization in the Watson IoT Platform.
    \ Various query\nparameters can be used to filter, sort and page through the list
    of\nschemas that are returned."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/schemas
  tags: Internet of Things,Draft,Schemas
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftschemas-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftschemas-get-openapi.md
- name: IBM Watson IoT Platform Create a draft schema definition
  x-api-slug: ibm-watson-iot-platform
  description: "Creates a new draft schema definition for the organization in the
    Watson\nIoT Platform.\n\nThe schema definition file is passed to the Watson IoT
    Platform within a\nmultipart POST (multipart/form-data).  The body of the POST
    **must**\ncontain at least two parts:\n\n  - One with a name of **schemaFile**
    that contains the actual content\n    of the file as the body of the part.\n    \n
    \ - One with a name of **name** that contains a string that defines the\n    name
    of the schema resource in the body of the part.\n\nAdditional metadata can be
    passed in other parts within the multipart\nPOST.  For example, to specify a description
    for the new schema\ndefinition, you should include a part with the name **description**
    and\nthe description as the body of the part.  To specify the type of the\nschema,
    you should include a part with the name **schemaType** and one\nof the following
    in the body of the part (the schemaType defaults to\njson-schema if the no schemaType
    part is present):\n\n  - json-schema\n\nIf parts with names other than those specified
    above are included in the\nmultipart POST the request will fail and an HTTP status
    code of 400 will\nbe returned.\n\nThe content of the schema definition file that
    is passed to the platform\nis stored and a REST resource is created containing
    metadata that\ndescribes the schema definition."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/schemas
  tags: Internet of Things,Draft,Schemas
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftschemas-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftschemas-post-openapi.md
- name: IBM Watson IoT Platform Get draft schema definition metadata
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieves the metadata for the draft schema definition with the
    specified id.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/schemas/{schemaId}
  tags: Internet of Things,Draft,Schemas,SchemaId
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftschemasschemaid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftschemasschemaid-get-openapi.md
- name: IBM Watson IoT Platform Update draft schema definition metadata
  x-api-slug: ibm-watson-iot-platform
  description: "Updates the metadata for the draft schema definition with the specified\nid.
    The following properties can be updated:\n\n  - name\n  - description\n  \nNote
    that if the description field is omitted from the body of the\nupdate, then any
    existing description will be removed from the schema\ndefinition.\n  \nAny changes
    made to the values of the following properties will be\nignored:\n\n  - schemaType\n
    \ - schemaFilename\n  - contentType\n  - created\n  - createdBy\n  - updated\n
    \ - updatedBy\n  - refs\n  \nThe schemaFilename and contentType properties are
    updated when the\ncontent of the schema file is updated.\n\nThe values of the
    created, createdBy, updated, updatedBy and refs\nproperties are set on the server
    as a result of a successful update."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/schemas/{schemaId}
  tags: Internet of Things,Draft,Schemas,SchemaId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftschemasschemaid-put-openapi.md
- name: IBM Watson IoT Platform Delete a draft schema definition
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Deletes the draft schema definition with the specified id from the
    organization in the Watson IoT Platform.  Deleting the schema definition
    deletes both the metadata and the actual schema definition file from the
    Watson IoT Platform.

    Please note the the delete will fail if the draft schema definition is
    being referenced by an event type or logical interface.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/schemas/{schemaId}
  tags: Internet of Things,Draft,Schemas,SchemaId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftschemasschemaid-delete-openapi.md
- name: IBM Watson IoT Platform Get the contents of the draft schema definition file
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieves the content of the draft schema definition file with the
    specified id.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/schemas/{schemaId}/content
  tags: Internet of Things,Draft,Schemas,SchemaId,Content
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftschemasschemaidcontent-get-openapi.md
- name: IBM Watson IoT Platform Update the content of a draft schema definition file
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Updates the content of a draft schema definition file with the specified
    id.

    The schema definition file is passed to the Watson IoT Platform within a
    multipart POST (multipart/form-data).  The body of the POST **must**
    contain one part with a name of the **schemaFile** and the
    actual schema file as the body of the part.

    Please note that the schemaFilename and contentType properties of the
    schema definition will also be updated as a result of updating the
    content of the schema file.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/schemas/{schemaId}/content
  tags: Internet of Things,Draft,Schemas,SchemaId,Content
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftschemasschemaidcontent-put-openapi.md
- name: IBM Watson IoT Platform Query active event types
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Event types are used to model the events that are published to the
    Watson IoT Platform.  An event type must be created in an organization
    before more complex processing can be performed on the native event.

    The **/event/types** endpoint returns the list of all of the active
    event types that have been defined for the organization in the Watson
    IoT Platform.  Various query parameters can be used to filter, sort and
    page through the list of active event types that are returned.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//event/types
  tags: Internet of Things,Event,Types
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/eventtypes-get-openapi.md
- name: IBM Watson IoT Platform Get an active event type
  x-api-slug: ibm-watson-iot-platform
  description: Retrieve the active event type with the specified id.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//event/types/{eventTypeId}
  tags: Internet of Things,Event,Types,EventTypeId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/eventtypeseventtypeid-get-openapi.md
- name: IBM Watson IoT Platform Query draft event types
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Event types are used to model the events that are published to the
    Watson IoT Platform.  An event type must be created in an organization
    before more complex processing can be performed on the native event.

    The **/draft/event/types** endpoint returns the list of all of the draft
    event types that have been defined for the organization in the Watson
    IoT Platform.  Various query parameters can be used to filter, sort and
    page through the list of draft event types that are returned.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/event/types
  tags: Internet of Things,Draft,Event,Types
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/drafteventtypes-get-openapi.md
- name: IBM Watson IoT Platform Create a draft event type
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Creates a new draft event type for the organization in the Watson IoT
    Platform.  The draft event type must reference the schema definition
    that defines the structure of the inbound MQTT event.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/event/types
  tags: Internet of Things,Draft,Event,Types
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/drafteventtypes-post-openapi.md
- name: IBM Watson IoT Platform Get a draft event type
  x-api-slug: ibm-watson-iot-platform
  description: Retrieve the draft event type with the specified id.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/event/types/{eventTypeId}
  tags: Internet of Things,Draft,Event,Types,EventTypeId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/drafteventtypeseventtypeid-get-openapi.md
- name: IBM Watson IoT Platform Update a draft event type
  x-api-slug: ibm-watson-iot-platform
  description: "Updates the draft event type with the specified id. The following\nproperties
    can be updated:\n\n  - name\n  - description\n  - schemaId\n\nNote that if the
    description field is omitted from the body of the\nupdate, then any existing description
    will be removed from the event\ntype.\n  \nAny changes made to the values of the
    following properties will be\nignored:\n\n  - created\n  - createdBy\n  - updated\n
    \ - updatedBy\n  - refs\n  \nThe values of these properties are set on the server
    as a result of a\nsuccessful update."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/event/types/{eventTypeId}
  tags: Internet of Things,Draft,Event,Types,EventTypeId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/drafteventtypeseventtypeid-put-openapi.md
- name: IBM Watson IoT Platform Delete a draft event type
  x-api-slug: ibm-watson-iot-platform
  description: "Deletes the draft event type with the specified id from the organization\nin
    the Watson IoT Platform.\n\nPlease note the the delete will fail if the draft
    event type is being \nreferenced by a physical interface."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/event/types/{eventTypeId}
  tags: Internet of Things,Draft,Event,Types,EventTypeId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/drafteventtypeseventtypeid-delete-openapi.md
- name: IBM Watson IoT Platform Query active phyiscal interfaces
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Physical interfaces are used to model the interfaces between physical
    devices and the Watson IoT Platform.  A physical interface references
    event types.  Devices that implement a physical interface publish these
    events to the platform.

    The event types are referenced via a mapping that maps an event id to
    the id of an event type.  The event id corresponds to the MQTT topic
    that the event is published to by a device.

    The **physicalinterfaces** endpoint returns the list of all of the
    active physical interfaces that have been defined for the organization
    in the Watson IoT Platform.  Various query parameters can be used to
    filter, sort and page through the list of active physical interfaces
    that are returned.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//physicalinterfaces
  tags: Internet of Things,Physicalinterfaces
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/physicalinterfaces-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/physicalinterfaces-get-openapi.md
- name: IBM Watson IoT Platform Get an active physical interface
  x-api-slug: ibm-watson-iot-platform
  description: Retrieve the active physical interface with the specified id.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//physicalinterfaces/{physicalInterfaceId}
  tags: Internet of Things,Physicalinterfaces,PhysicalInterfaceId
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/physicalinterfacesphysicalinterfaceid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/physicalinterfacesphysicalinterfaceid-get-openapi.md
- name: IBM Watson IoT Platform Get the list of event mappings
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieve the list of event mappings for the active physical interface.
    Event mappings are keyed off of the event id specified in the MQTT topic
    that the inbound events are published to.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//physicalinterfaces/{physicalInterfaceId}/events
  tags: Internet of Things,Physicalinterfaces,PhysicalInterfaceId,Events
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/physicalinterfacesphysicalinterfaceidevents-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/physicalinterfacesphysicalinterfaceidevents-get-openapi.md
- name: IBM Watson IoT Platform Query draft phyiscal interfaces
  x-api-slug: ibm-watson-iot-platform
  description: "Physical interfaces are used to model the interfaces between physical\ndevices
    and the Watson IoT Platform.  A physical interface references\nevent types.  Devices
    that implement a physical interface publish these\nevents to the platform.\n\nThe
    event types are referenced via a mapping that maps an event id to\nthe id of an
    event type.  The event id corresponds to the MQTT topic\nthat the event is published
    to by a device.\n\nThe **/draft/physicalinterfaces** endpoint returns the list
    of all of \nthe draft physical interfaces that have been defined for the\norganization
    in the Watson IoT Platform.  Various query parameters can\nbe used to filter,
    sort and page through the list of draft physical\ninterfaces that are returned."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/physicalinterfaces
  tags: Internet of Things,Draft,Physicalinterfaces
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftphysicalinterfaces-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftphysicalinterfaces-get-openapi.md
- name: IBM Watson IoT Platform Create a draft physical interface
  x-api-slug: ibm-watson-iot-platform
  description: "Creates a new draft physical interface for the organization in the
    \nWatson IoT Platform."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/physicalinterfaces
  tags: Internet of Things,Draft,Physicalinterfaces
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftphysicalinterfaces-post-openapi.md
- name: IBM Watson IoT Platform Get a draft physical interface
  x-api-slug: ibm-watson-iot-platform
  description: Retrieve the draft physical interface with the specified id.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/physicalinterfaces/{physicalInterfaceId}
  tags: Internet of Things,Draft,Physicalinterfaces,PhysicalInterfaceId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftphysicalinterfacesphysicalinterfaceid-get-openapi.md
- name: IBM Watson IoT Platform Update a draft physical interface
  x-api-slug: ibm-watson-iot-platform
  description: "Updates the draft physical interface with the specified id. The \nfollowing
    properties can be updated:\n\n  - name\n  - description\n\nNote that if the description
    field is omitted from the body of the\nupdate, then any existing description will
    be removed from the physical\ninterface.\n  \nAny changes made to the values of
    the following properties will be\nignored:\n\n  - created\n  - createdBy\n  -
    updated\n  - updatedBy\n  - refs\n  \nThe values of these properties are set on
    the server as a result of a\nsuccessful update."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/physicalinterfaces/{physicalInterfaceId}
  tags: Internet of Things,Draft,Physicalinterfaces,PhysicalInterfaceId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftphysicalinterfacesphysicalinterfaceid-put-openapi.md
- name: IBM Watson IoT Platform Delete a draft physical interface
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Deletes the draft physical interface with the specified id from the
    organization in the Watson IoT Platform.

    Please note the the delete will fail if the draft physical interface is
    being referenced  by a device type.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/physicalinterfaces/{physicalInterfaceId}
  tags: Internet of Things,Draft,Physicalinterfaces,PhysicalInterfaceId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftphysicalinterfacesphysicalinterfaceid-delete-openapi.md
- name: IBM Watson IoT Platform Get the list of event mappings
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieve the list of event mappings for the draft physical interface.
    Event mappings are keyed off of the event id specified in the MQTT topic
    that the inbound events are published to.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/physicalinterfaces/{physicalInterfaceId}/events
  tags: Internet of Things,Draft,Physicalinterfaces,PhysicalInterfaceId,Events
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftphysicalinterfacesphysicalinterfaceidevents-get-openapi.md
- name: IBM Watson IoT Platform Map an event to the draft physical interface
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Maps an event id to a specific event type for the draft specified
    physical interface.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/physicalinterfaces/{physicalInterfaceId}/events
  tags: Internet of Things,Draft,Physicalinterfaces,PhysicalInterfaceId,Events
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftphysicalinterfacesphysicalinterfaceidevents-post-openapi.md
- name: IBM Watson IoT Platform Remove an event mapping from the draft physical interface
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Removes the event mapping with the specified id from the draft physical
    interface.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/physicalinterfaces/{physicalInterfaceId}/events/{eventId}
  tags: Internet of Things,Draft,Physicalinterfaces,PhysicalInterfaceId,Events,EventId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftphysicalinterfacesphysicalinterfaceideventseventid-delete-openapi.md
- name: IBM Watson IoT Platform Query active logical interfaces
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Logical interfaces are used to model the interfaces exposed by a
    device or thing in the Watson IoT Platform. A logical interface
    must reference a schema definition that defines the structure of the
    state that will be stored for the device or thing.

    The **logicalinterfaces** endpoint returns the list of all of the
    active logical interfaces that have been defined for the organization
    in the Watson IoT Platform.  Various query parameters can
    be used to filter, sort and page through the list of active logical
    interfaces that are returned.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//logicalinterfaces
  tags: Internet of Things,Logical interfaces
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/logicalinterfaces-get-openapi.md
- name: IBM Watson IoT Platform Get an active logical interface
  x-api-slug: ibm-watson-iot-platform
  description: Retrieve the active logical interface with the specified id.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//logicalinterfaces/{logicalInterfaceId}
  tags: Internet of Things,Logical interfaces,LogicalInterfaceId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/logicalinterfaceslogicalinterfaceid-get-openapi.md
- name: IBM Watson IoT Platform Perform an operation against a logical interface
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Performs the specified operation against the logical interface. The
    following values can be specified for the operation property:

      - deactivate-configuration

    The **deactivate-configuration** operation will remove any active
    configuration that is currently associated with the logical
    interface. If the logical interface is associated with any device
    types, the state for any instances of those device types will be deleted
    as a result of performing the **deactivate-configuration** operation.
    The **deactivate-configuration** operation will fail if the logical
    interface is referenced by a thing schema.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//logicalinterfaces/{logicalInterfaceId}
  tags: Internet of Things,Logical interfaces,LogicalInterfaceId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/logicalinterfaceslogicalinterfaceid-patch-openapi.md
- name: IBM Watson IoT Platform Query draft logical interfaces
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Logical interfaces are used to model the interfaces exposed by a
    device or thing in the Watson IoT Platform. A logical interface must
    reference a schema definition that defines the structure of the
    state that will be stored for the device or thing.

    The **logicalinterfaces** endpoint returns the list of all of the
    draft logical interfaces that have been defined for the organization
    in the Watson IoT Platform.  Various query parameters can be used to
    filter, sort and page through the list of draft logical interfaces
    that are returned.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/logicalinterfaces
  tags: Internet of Things,Draft,Logical interfaces
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftlogicalinterfaces-get-openapi.md
- name: IBM Watson IoT Platform Create a draft logical interface
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Creates a new draft logical interface for the organization in the
    Watson IoT Platform. The logical interface must reference a schema
    definition that defines the structure of the state that will be stored
    for the device or thing.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/logicalinterfaces
  tags: Internet of Things,Draft,Logical interfaces
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftlogicalinterfaces-post-openapi.md
- name: IBM Watson IoT Platform Get a draft logical interface
  x-api-slug: ibm-watson-iot-platform
  description: Retrieve the draft logical interface with the specified id.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/logicalinterfaces/{logicalInterfaceId}
  tags: Internet of Things,Draft,Logical interfaces,LogicalInterfaceId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftlogicalinterfaceslogicalinterfaceid-get-openapi.md
- name: IBM Watson IoT Platform Update a draft logical interface
  x-api-slug: ibm-watson-iot-platform
  description: "Updates the draft logical interface with the specified id. The\nfollowing
    properties can be updated: \n\n  - name\n  - description\n  - schemaId\n\nNote
    that if the description field is omitted from the body of the\nupdate, then any
    existing description will be removed from the logical\ninterface.\n  \nAny changes
    made to the values of the following properties will be\nignored:\n\n  - created\n
    \ - createdBy\n  - updated\n  - updatedBy\n  - refs\n  \nThe values of these properties
    are set on the server as a result of a\nsuccessful update."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/logicalinterfaces/{logicalInterfaceId}
  tags: Internet of Things,Draft,Logical interfaces,LogicalInterfaceId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftlogicalinterfaceslogicalinterfaceid-put-openapi.md
- name: IBM Watson IoT Platform Perform an operation against a draft logical interface
  x-api-slug: ibm-watson-iot-platform
  description: "Performs the specified operation against the draft logical\ninterface.
    The following values can be specified for the operation\nproperty:\n\n  - validate-configuration\n
    \ - activate-configuration\n  - list-differences\n\nThe **validate-configuration**
    operation will analyze all of the \nconfiguration associated with the draft logical
    interface to\ndetermine if it is valid.  If the configuration is invalid, a list
    of \nthe issues will be returned in the body of the response.  \n \nThe **activate-configuration**
    operation will make the configuration\nassociated with the draft logical interface
    active. The \n**activate-configuration** operation must have been performed against\na
    draft logical interface before any state is generated for device\nor thing types
    that are associated with that logical interface.\n\nThe **list-differences** operation
    will return a list of the differences\nthat exist between the active configuration
    for the logical\ninterface, if any, and the draft configuration."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/logicalinterfaces/{logicalInterfaceId}
  tags: Internet of Things,Draft,Logical interfaces,LogicalInterfaceId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftlogicalinterfaceslogicalinterfaceid-patch-openapi.md
- name: IBM Watson IoT Platform Delete a draft logical interface
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Deletes the draft logical interface with the specified id from the
    organization in the Watson IoT Platform.

    Please note the the delete will fail if the draft logical interface
    is being referenced by a device type.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/logicalinterfaces/{logicalInterfaceId}
  tags: Internet of Things,Draft,Logical interfaces,LogicalInterfaceId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftlogicalinterfaceslogicalinterfaceid-delete-openapi.md
- name: IBM Watson IoT Platform Query active rules
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Rules allow you to specify conditions that can be used to trigger
    actions. For example, you might create a rule that sends an email if
    the temperature of a device exceeds a certain value.

    Rules are defined against a specific logical interface schema.  At
    runtime, a rule will be evaluated whenever the state for a Device that
    exposes the logical interface changes.

    The **/logicalinterfaces/{logicalInterfaceId}/rules** endpoint returns
    the list of all of the active rules that have been associated with the
    logical interface. Various query parameters can be used to filter, sort
    and page through the list of rules that are returned.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//logicalinterfaces/{logicalInterfaceId}/rules
  tags: Internet of Things,Logical interfaces,LogicalInterfaceId,Rules
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/logicalinterfaceslogicalinterfaceidrules-get-openapi.md
- name: IBM Watson IoT Platform Get an active rule
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieve the active rule with the specified id that has been associated
    with the specified logical interface.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//logicalinterfaces/{logicalInterfaceId}/rules/{ruleId}
  tags: Internet of Things,Logical interfaces,LogicalInterfaceId,Rules,RuleId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/logicalinterfaceslogicalinterfaceidrulesruleid-get-openapi.md
- name: IBM Watson IoT Platform Query draft rules
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Rules allow you to specify conditions that can be used to trigger
    actions. For example, you might create a rule that sends an email if
    the temperature of a device exceeds a certain value.

    Rules are defined against a specific logical interface schema.  At
    runtime, a rule will be evaluated whenever the state for a Device that
    exposes the logical interface changes.

    The **/draft/logicalinterfaces/{logicalInterfaceId}/rules** endpoint
    returns the list of all of the draft rules that have been associated
    with the logical interface. Various query parameters can be used to
    filter, sort and page through the list of rules that are returned.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/logicalinterfaces/{logicalInterfaceId}/rules
  tags: Internet of Things,Draft,Logical interfaces,LogicalInterfaceId,Rules
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftlogicalinterfaceslogicalinterfaceidrules-get-openapi.md
- name: IBM Watson IoT Platform Create a draft rule
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Creates a new draft rule that is associated with the logical interface
    for the organization in the Watson IoT Platform.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/logicalinterfaces/{logicalInterfaceId}/rules
  tags: Internet of Things,Draft,Logical interfaces,LogicalInterfaceId,Rules
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftlogicalinterfaceslogicalinterfaceidrules-post-openapi.md
- name: IBM Watson IoT Platform Get a draft rule
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieve the draft rule with the specified id that has been associated
    with the specified logical interface.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/logicalinterfaces/{logicalInterfaceId}/rules/{ruleId}
  tags: Internet of Things,Draft,Logical interfaces,LogicalInterfaceId,Rules,RuleId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftlogicalinterfaceslogicalinterfaceidrulesruleid-get-openapi.md
- name: IBM Watson IoT Platform Update a draft rule
  x-api-slug: ibm-watson-iot-platform
  description: "Updates the draft rule with the specified id. The following properties\ncan
    be updated: \n\n  - name\n  - description\n  - condition\n\nNote that if the description
    field is omitted from the body of the\nupdate, then any existing description will
    be removed from the rule.\n  \nAny changes made to the values of the following
    properties will be\nignored:\n\n  - created\n  - createdBy\n  - updated\n  - updatedBy\n
    \ - refs\n  \nThe values of these properties are set on the server as a result
    of a\nsuccessful update."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/logicalinterfaces/{logicalInterfaceId}/rules/{ruleId}
  tags: Internet of Things,Draft,Logical interfaces,LogicalInterfaceId,Rules,RuleId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftlogicalinterfaceslogicalinterfaceidrulesruleid-put-openapi.md
- name: IBM Watson IoT Platform Delete a draft rule
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Deletes the draft rule with the specified id from the organization in
    the Watson IoT Platform.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/logicalinterfaces/{logicalInterfaceId}/rules/{ruleId}
  tags: Internet of Things,Draft,Logical interfaces,LogicalInterfaceId,Rules,RuleId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftlogicalinterfaceslogicalinterfaceidrulesruleid-delete-openapi.md
- name: IBM Watson IoT Platform List device types
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Sorting can be performed on any of the following properties (sort
    order can be reversed by prefixing the property name with '-'):
    - id
    - description
    - deviceInfo.description
    - deviceInfo.descriptiveLocation
    - deviceInfo.serialNumber
    - deviceInfo.deviceClass
    - deviceInfo.fwVersion
    - deviceInfo.hwVersion
    - deviceInfo.manufacturer
    - deviceInfo.model

    The following facets are supported:
    - deviceInfo.deviceClass
    - deviceInfo.fwVersion
    - deviceInfo.hwVersion
    - deviceInfo.manufacturer
    - deviceInfo.model
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//device/types
  tags: Internet of Things,Device,Types
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/devicetypes-get-openapi.md
- name: IBM Watson IoT Platform Perform an operation against a device type
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Performs the specified operation against the device type. The following
    values can be specified for the operation property:

      - deactivate-configuration

    The **deactivate-configuration** operation will remove any activate
    configuration that is currently associated with the device type. If any
    instances of the device type exist, the state for those devices will be
    deleted as a result of performing the **deactivate-configuration**
    operation. The **deactivate-configuration** operation will fail if
    any instances of the device type are being aggregated into an instance
    of a thing.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//device/types/{typeId}
  tags: Internet of Things,Device,Types
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/devicetypestypeid-patch-openapi.md
- name: IBM Watson IoT Platform Get the active physical interface associated with
    the device type
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieve the active physical interface that has been associated with the
    device type.  At least one active physical interface must be associated
    with the device type before any mappings can be defined that will
    generate state for the device.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//device/types/{typeId}/physicalinterface
  tags: Internet of Things,Device,Types,Physicalinterface
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/devicetypestypeidphysicalinterface-get-openapi.md
- name: |-
    IBM Watson IoT Platform Get the list of active logical interfaces associated with the device
    type
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieve the list of active logical interfaces that have been
    associated with the device type.  At least one logical interface
    must be associated with the device type before any mappings can be
    defined that will generate state for the device.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//device/types/{typeId}/logicalinterfaces
  tags: Internet of Things,Device,Types,Logical interfaces
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/devicetypestypeidlogicalinterfaces-get-openapi.md
- name: IBM Watson IoT Platform Get the list of active property mappings for the device
    type
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieve the list of active property mappings for the specified device
    type.  A property mapping defines how properties from inbound events are
    mapped to properties defined on an logical interface associated with
    the device type.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//device/types/{typeId}/mappings
  tags: Internet of Things,Device,Types,Mappings
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/devicetypestypeidmappings-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/devicetypestypeidmappings-get-openapi.md
- name: |-
    IBM Watson IoT Platform Get the active property mappings for a specific logical interface
    for a device type.
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieves the active property mappings for a specific logical
    interface for the device type.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//device/types/{typeId}/mappings/{logicalInterfaceId}
  tags: Internet of Things,Device,Types,Mappings,LogicalInterfaceId
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/devicetypestypeidmappingslogicalinterfaceid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/devicetypestypeidmappingslogicalinterfaceid-get-openapi.md
- name: IBM Watson IoT Platform List device types associated with an logical or physical
    interface
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieves the list of device types that are associated with the
    logical interface and/or physical interface with the ids specified
    using the corresponding query parameters.

    Note that at least one of the following query parameters must be
    specified:

      - logicalInterfaceId
      - physicalInterfaceId
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/device/types
  tags: Internet of Things,Draft,Device,Types
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftdevicetypes-get-openapi.md
- name: IBM Watson IoT Platform Perform an operation against a draft device type
  x-api-slug: ibm-watson-iot-platform
  description: "Performs the specified operation against the draft device type. The\nfollowing
    values can be specified for the operation property:\n\n  - validate-configuration\n
    \ - activate-configuration\n  - list-differences\n\nThe **validate-configuration**
    operation will analyze all of the \nconfiguration associated with the draft device
    type to determine if it\nis valid.  If the configuration is invalid, a list of
    the issues will\nbe returned in the body of the response.  \n \nThe **activate-configuration**
    operation will make the configuration\nassociated with the draft device type active.
    The\n**activate-configuration** operation must have been performed against a\ndraft
    device type before any state is generated for instances of that\ntype.\n\nThe
    **list-differences** operation will return a list of the differences\nthat exist
    between the active configuration for the device type, if\nany, and the draft configuration."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/device/types/{typeId}
  tags: Internet of Things,Draft,Device,Types
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftdevicetypestypeid-patch-openapi.md
- name: IBM Watson IoT Platform Get the draft physical interface associated with the
    device type
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieve the draft physical interface that has been associated with the
    device type.  At least one active physical interface must be associated
    with the device type before any mappings can be defined that will
    generate state for the device.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/device/types/{typeId}/physicalinterface
  tags: Internet of Things,Draft,Device,Types,Physicalinterface
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftdevicetypestypeidphysicalinterface-get-openapi.md
- name: IBM Watson IoT Platform Associate a draft physical interface with the device
    type
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Associates a draft physical interface with the specified device type.
    The draft physical interface must already exist within the organization
    in the Watson IoT Platform. If a draft physical interface is already
    associated with the device type it will be replaced with the specified
    physical interface.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/device/types/{typeId}/physicalinterface
  tags: Internet of Things,Draft,Device,Types,Physicalinterface
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftdevicetypestypeidphysicalinterface-post-openapi.md
- name: IBM Watson IoT Platform Disassociate the draft physical interface from the
    device type
  x-api-slug: ibm-watson-iot-platform
  description: Disassociates the draft physical interface from the device type.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/device/types/{typeId}/physicalinterface
  tags: Internet of Things,Draft,Device,Types,Physicalinterface
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftdevicetypestypeidphysicalinterface-delete-openapi.md
- name: |-
    IBM Watson IoT Platform Get the list of draft logical interfaces associated with the device
    type
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieve the list of draft logical interfaces that have been
    associated with the device type.  At least one active logical
    interface must be associated with the device type before any mappings
    can be defined that will generate state for the device.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/device/types/{typeId}/logicalinterfaces
  tags: Internet of Things,Draft,Device,Types,Logical interfaces
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftdevicetypestypeidlogicalinterfaces-get-openapi.md
- name: IBM Watson IoT Platform Associate a draft logical interface with the device
    type
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Associates a draft logical interface with the specified device type.
    The draft logical interface must already exist within the organization
    in the Watson IoT Platform.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/device/types/{typeId}/logicalinterfaces
  tags: Internet of Things,Draft,Device,Types,Logical interfaces
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftdevicetypestypeidlogicalinterfaces-post-openapi.md
- name: IBM Watson IoT Platform Disassociate a draft logical interface from the device
    type
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Disassociates the draft logical interface  with the specified id
    from the device type.

    Please note the the delete will fail if the draft logical interface
    being removed from the device type is referenced in the property
    mappings for the device type.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/device/types/{typeId}/logicalinterfaces/{logicalInterfaceId}
  tags: Internet of Things,Draft,Device,Types,Logical interfaces,LogicalInterfaceId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftdevicetypestypeidlogicalinterfaceslogicalinterfaceid-delete-openapi.md
- name: IBM Watson IoT Platform Get the list of draft property mappings for the device
    type
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieve the list of draft property mappings for the specified device
    type.  A property mapping defines how properties from inbound events are
    mapped to properties defined on an logical interface associated with
    the device type.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/device/types/{typeId}/mappings
  tags: Internet of Things,Draft,Device,Types,Mappings
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftdevicetypestypeidmappings-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftdevicetypestypeidmappings-get-openapi.md
- name: |-
    IBM Watson IoT Platform Create the draft property mappings for a logical interface for the
    device type
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Creates the draft property mappings for an logical interface for the
    device type.  The mapping object must specify:
    - The id for for the logical interface that the mappings are for
    - The mappings that define how to map from properties on the inbound
      events to the properties on the logical interface.  The mappings
      are keyed off of the event ids defined by the physical interface
      associated with the device type.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/device/types/{typeId}/mappings
  tags: Internet of Things,Draft,Device,Types,Mappings
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftdevicetypestypeidmappings-post-openapi.md
- name: |-
    IBM Watson IoT Platform Get the draft property mappings for a specific logical interface for
    a device type.
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieves the draft property mappings for a specific logical
    interface for the device type.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/device/types/{typeId}/mappings/{logicalInterfaceId}
  tags: Internet of Things,Draft,Device,Types,Mappings,LogicalInterfaceId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftdevicetypestypeidmappingslogicalinterfaceid-get-openapi.md
- name: |-
    IBM Watson IoT Platform Update the draft property mappings for a specific logical interface
    for the device type.
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Updates the draft property mappings for a specific logical interface
    for the device type.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/device/types/{typeId}/mappings/{logicalInterfaceId}
  tags: Internet of Things,Draft,Device,Types,Mappings,LogicalInterfaceId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftdevicetypestypeidmappingslogicalinterfaceid-put-openapi.md
- name: |-
    IBM Watson IoT Platform Delete the draft property mappings for a specific logical interface
    for the device type.
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Deletes the draft property mappings for a specific logical interface
    for the device type.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/device/types/{typeId}/mappings/{logicalInterfaceId}
  tags: Internet of Things,Draft,Device,Types,Mappings,LogicalInterfaceId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftdevicetypestypeidmappingslogicalinterfaceid-delete-openapi.md
- name: IBM Watson IoT Platform Get the state for the device with the specified id
  x-api-slug: ibm-watson-iot-platform
  description: Retrieve the current state of the device with the specified id.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//device/types/{typeId}/devices/{deviceId}/state/{logicalInterfaceId}
  tags: Internet of Things,Device,Types,Devices,DeviceId,State,LogicalInterfaceId
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/devicetypestypeiddevicesdeviceidstatelogicalinterfaceid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/devicetypestypeiddevicesdeviceidstatelogicalinterfaceid-get-openapi.md
- name: IBM Watson IoT Platform Perform an operation against the device state for
    a logical interface
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Performs the specified operation against the device state for a logical
    interface. The following values can be specified for the operation
    property:

      - reset-state

    The **reset-state** operation will reset the state of the specified
    device to the default values as defined by the schema for the logical
    interface.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//device/types/{typeId}/devices/{deviceId}/state/{logicalInterfaceId}
  tags: Internet of Things,Device,Types,Devices,DeviceId,State,LogicalInterfaceId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/devicetypestypeiddevicesdeviceidstatelogicalinterfaceid-patch-openapi.md
- name: IBM Watson IoT Platform Query active thing types
  x-api-slug: ibm-watson-iot-platform
  description: "Within the Watson IoT Platform, a Thing allows you to aggregate one
    or\nmore instances of a Device or Thing together to represent a more coarse\ngrained
    object.  For example, you might aggregrate together a temperature\nsensor, flow
    sensor and power sensor together into a Boiler. \n\nThing Types are used to model
    Things.  The Schema associated with a\nThing Type defines the type of objects
    that are aggregated togther to\nmake up an instance of a Thing. A Thing Type must
    be created in an \norganization before in instance of a Thing can be created.\n\nThe
    **/thing/types** endpoint returns the list of all of the active\nThing types that
    have been defined for the organization in the Watson IoT\nPlatform. Various query
    parameters can be used to filter, sort and page\nthrough the list of Thing types
    that are returned."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//thing/types
  tags: Internet of Things,Thing,Types
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/thingtypes-get-openapi.md
- name: IBM Watson IoT Platform Get an active thing type
  x-api-slug: ibm-watson-iot-platform
  description: Retrieve the active thing type with the specified id.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//thing/types/{thingTypeId}
  tags: Internet of Things,Thing,Types,ThingTypeId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/thingtypesthingtypeid-get-openapi.md
- name: IBM Watson IoT Platform Perform an operation against an active thing type
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Performs the specified operation against the active thing type. The
    following values can be specified for the operation property:

      - deactivate-configuration

    The **deactivate-configuration** operation will remove any active
    configuration that is currently associated with the thing type. The
    **deactivate-configuration** operation will fail if there are
    any instances of the thing type.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//thing/types/{thingTypeId}
  tags: Internet of Things,Thing,Types,ThingTypeId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/thingtypesthingtypeid-patch-openapi.md
- name: IBM Watson IoT Platform Query draft thing types
  x-api-slug: ibm-watson-iot-platform
  description: "Within the Watson IoT Platform, a Thing allows you to aggregate one
    or\nmore instances of a Device or Thing together to represent a more coarse\ngrained
    object.  For example, you might aggregrate together a temperature\nsensor, flow
    sensor and power sensor together into a Boiler. \n\nThing Types are used to model
    Things.  The Schema associated with a\nThing Type defines the type of objects
    that are aggregated togther to\nmake up an instance of a Thing. A Thing Type must
    be created in an \norganization before in instance of a Thing can be created.\n\nThe
    **/draft/thing/types** endpoint returns the list of all of the draft\nThing types
    that have been defined for the organization in the Watson IoT\nPlatform. Various
    query parameters can be used to filter, sort and page\nthrough the list of draft
    Thing types that are returned."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/thing/types
  tags: Internet of Things,Draft,Thing,Types
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftthingtypes-get-openapi.md
- name: IBM Watson IoT Platform Create a draft thing type
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Creates a new draft thing type for the organization in the Watson IoT
    Platform.  The thing type must reference the schema definition that
    defines the structure of instances of the thing type.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/thing/types
  tags: Internet of Things,Draft,Thing,Types
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftthingtypes-post-openapi.md
- name: IBM Watson IoT Platform Get a draft thing type
  x-api-slug: ibm-watson-iot-platform
  description: Retrieve the draft thing type with the specified id.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/thing/types/{thingTypeId}
  tags: Internet of Things,Draft,Thing,Types,ThingTypeId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftthingtypesthingtypeid-get-openapi.md
- name: IBM Watson IoT Platform Update a draft thing type
  x-api-slug: ibm-watson-iot-platform
  description: "Updates the draft thing type with the specified id. The following\nproperties
    can be updated:\n\n  - name\n  - description\n  - schemaId\n  - metadata\n\nNote
    that if the description field is omitted from the body of the\nupdate, then any
    existing description will be removed from the draft\nthing type.\n  \nAny changes
    made to the values of the following properties will be\nignored:\n\n  - version\n
    \ - created\n  - createdBy\n  - updated\n  - updatedBy\n  - refs\n  \nThe values
    of these properties are set on the server as a result of a\nsuccessful update."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/thing/types/{thingTypeId}
  tags: Internet of Things,Draft,Thing,Types,ThingTypeId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftthingtypesthingtypeid-put-openapi.md
- name: IBM Watson IoT Platform Perform an operation against a draft thing type
  x-api-slug: ibm-watson-iot-platform
  description: "Performs the specified operation against the draft thing type. The\nfollowing
    values can be specified for the operation property:\n\n  - validate-configuration\n
    \ - activate-configuration\n  - list-differences\n\nThe **validate-configuration**
    operation will analyze all of the \nconfiguration associated with the draft thing
    type to determine if it is\nvalid.  If the configuration is invalid, a list of
    the issues will be\nreturned in the body of the response.  \n \nThe **activate-configuration**
    operation will make the configuration\nassociated with the draft thing type active.
    The \n**activate-configuration** operation must have been performed against a\ndraft
    thing type before any instances of that type can be created.\n\nThe **list-differences**
    operation will return a list of the differences\nthat exist between the active
    configuration for the thing type, if any,\nand the draft configuration."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/thing/types/{thingTypeId}
  tags: Internet of Things,Draft,Thing,Types,ThingTypeId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftthingtypesthingtypeid-patch-openapi.md
- name: IBM Watson IoT Platform Delete a draft thing type
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Deletes the draft thing type with the specified id from the organization
    in the Watson IoT Platform.

    Please note the the delete will fail if there is an active version of the
    thing type or if the thing type is currently being referenced by another
    object.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/thing/types/{thingTypeId}
  tags: Internet of Things,Draft,Thing,Types,ThingTypeId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftthingtypesthingtypeid-delete-openapi.md
- name: |-
    IBM Watson IoT Platform Get the list of active logical interfaces associated with the thing
    type
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieve the list of active logical  interfaces that have been associated
    with the thing type.  At least one logical interface must be associated
    with the thing type before any mappings can be defined that will generate
    state for the thing.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//thing/types/{thingTypeId}/logicalinterfaces
  tags: Internet of Things,Thing,Types,ThingTypeId,Logical interfaces
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/thingtypesthingtypeidlogicalinterfaces-get-openapi.md
- name: IBM Watson IoT Platform Get the list of active property mappings for the thing
    type
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieve the list of active property mappings for the specified thing
    type.  A property mapping defines how properties from state update events
    on aggregated devices or things are mapped to properties defined on a
    logical interface associated with the thing type.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//thing/types/{thingTypeId}/mappings
  tags: Internet of Things,Thing,Types,ThingTypeId,Mappings
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/thingtypesthingtypeidmappings-get-openapi.md
- name: |-
    IBM Watson IoT Platform Get the active property mappings for a specific logical interface for
    a thing type.
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieves the active property mappings for a specific logical interface
    for the thing type.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//thing/types/{thingTypeId}/mappings/{logicalInterfaceId}
  tags: Internet of Things,Thing,Types,ThingTypeId,Mappings,LogicalInterfaceId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/thingtypesthingtypeidmappingslogicalinterfaceid-get-openapi.md
- name: |-
    IBM Watson IoT Platform Get the list of draft logical interfaces associated with the thing
    type
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieve the list of draft logical interfaces that have been associated
    with the draft thing type.  At least one logical interface must be
    associated with the thing type before any mappings can be defined that
    will generate state for the thing.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/thing/types/{thingTypeId}/logicalinterfaces
  tags: Internet of Things,Draft,Thing,Types,ThingTypeId,Logical interfaces
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftthingtypesthingtypeidlogicalinterfaces-get-openapi.md
- name: IBM Watson IoT Platform Associate a draft logical interface with the draft
    thing type
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Associates a draft logical interface with the specified draft thing type.
    The logical interface must already exist within the organization in the
    Watson IoT Platform.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/thing/types/{thingTypeId}/logicalinterfaces
  tags: Internet of Things,Draft,Thing,Types,ThingTypeId,Logical interfaces
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftthingtypesthingtypeidlogicalinterfaces-post-openapi.md
- name: IBM Watson IoT Platform Disassociate a logical interface from the draft thing
    type
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Disassociates the draft logical interface with the specified id from the
    draft thing type.

    Please note the the delete will fail if the logical interface being
    removed from the draft thing type is referenced in the property mappings
    for the draft thing type.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/thing/types/{thingTypeId}/logicalinterfaces/{logicalInterfaceId}
  tags: Internet of Things,Draft,Thing,Types,ThingTypeId,Logical interfaces,LogicalInterfaceId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftthingtypesthingtypeidlogicalinterfaceslogicalinterfaceid-delete-openapi.md
- name: IBM Watson IoT Platform Get the list of draft property mappings for the thing
    type
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieve the list of draft property mappings for the specified draft
    thing type.  A property mapping defines how properties from state update
    events on aggregated devices or things are mapped to properties defined
    on a logical interface associated with the thing type.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/thing/types/{thingTypeId}/mappings
  tags: Internet of Things,Draft,Thing,Types,ThingTypeId,Mappings
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftthingtypesthingtypeidmappings-get-openapi.md
- name: |-
    IBM Watson IoT Platform Create the draft property mappings for a logical interface for the thing
    type
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Creates the draft property mappings for a logical interface for the
    thing type.  The mapping object must specify:
    - The id for for the logical interface that the mappings are for
    - The mappings that define how to map from properties on the state
      update events to the properties on the logical interface.  The
      mappings are keyed off of the name of the internal properties of the
      thing type.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/thing/types/{thingTypeId}/mappings
  tags: Internet of Things,Draft,Thing,Types,ThingTypeId,Mappings
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftthingtypesthingtypeidmappings-post-openapi.md
- name: |-
    IBM Watson IoT Platform Get the draft property mappings for a specific logical interface for
    a thing type.
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieves the draft property mappings for a specific logical interface
    for the thing type.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/thing/types/{thingTypeId}/mappings/{logicalInterfaceId}
  tags: Internet of Things,Draft,Thing,Types,ThingTypeId,Mappings,LogicalInterfaceId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftthingtypesthingtypeidmappingslogicalinterfaceid-get-openapi.md
- name: |-
    IBM Watson IoT Platform Update the property mappings for a specific logical interface for
    the thing type.
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Updates the property mappings for a specific logical interface
    for the draft thing type.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/thing/types/{thingTypeId}/mappings/{logicalInterfaceId}
  tags: Internet of Things,Draft,Thing,Types,ThingTypeId,Mappings,LogicalInterfaceId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftthingtypesthingtypeidmappingslogicalinterfaceid-put-openapi.md
- name: |-
    IBM Watson IoT Platform Delete the property mappings for a specific logical interface for
    the draft thing type.
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Deletes the property mappings for a specific logical interface
    for the draft thing type.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/thing/types/{thingTypeId}/mappings/{logicalInterfaceId}
  tags: Internet of Things,Draft,Thing,Types,ThingTypeId,Mappings,LogicalInterfaceId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/draftthingtypesthingtypeidmappingslogicalinterfaceid-delete-openapi.md
- name: IBM Watson IoT Platform List things
  x-api-slug: ibm-watson-iot-platform
  description: "Within the Watson IoT Platform, a Thing allows you to aggregate one
    or\nmore instances of a Device or Thing together to represent a more coarse\ngrained
    object.  For example, you might aggregrate together a\ntemperature sensor, flow
    sensor and power sensor together into a Boiler. \n\nThe **/thing/types/{thingTypeId}/things**
    endpoint returns the list of\nall of the Thing instances of the specified type
    that have been created\nfor the organization in the Watson IoT Platform. Various
    query\nparameters can be used to filter, sort and page through the list of\nThing
    instances that are returned."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//thing/types/{thingTypeId}/things
  tags: Internet of Things,Thing,Types,ThingTypeId,Things
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/thingtypesthingtypeidthings-get-openapi.md
- name: IBM Watson IoT Platform Create a thing
  x-api-slug: ibm-watson-iot-platform
  description: "Creates a thing instance of the specified type for the organization
    in\nthe Watson IoT Platform. The thing type must have a valid set of   \nInformation
    Management metadata associated with it and activated before\nany instances can
    be created."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//thing/types/{thingTypeId}/things
  tags: Internet of Things,Thing,Types,ThingTypeId,Things
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/thingtypesthingtypeidthings-post-openapi.md
- name: IBM Watson IoT Platform Get a thing
  x-api-slug: ibm-watson-iot-platform
  description: Retrieve the thing with the specified id.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//thing/types/{thingTypeId}/things/{thingId}
  tags: Internet of Things,Thing,Types,ThingTypeId,Things,ThingId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/thingtypesthingtypeidthingsthingid-get-openapi.md
- name: IBM Watson IoT Platform Update a thing
  x-api-slug: ibm-watson-iot-platform
  description: "Updates the thing with the specified id. The following properties\ncan
    be updated:\n\n  - name\n  - description\n  - metadata\n  - aggregatedObjects\n\nNote
    that if the description field is omitted from the body of the\nupdate, then any
    existing description will be removed from the thing\ntype.\n  \nAny changes made
    to the values of the following properties will be\nignored:\n\n  - created\n  -
    createdBy\n  - updated\n  - updatedBy\n  \nThe values of these properties are
    set on the server as a result of a\nsuccessful update."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//thing/types/{thingTypeId}/things/{thingId}
  tags: Internet of Things,Thing,Types,ThingTypeId,Things,ThingId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/thingtypesthingtypeidthingsthingid-put-openapi.md
- name: IBM Watson IoT Platform Delete a thing
  x-api-slug: ibm-watson-iot-platform
  description: "Deletes the thing with the specified id from the organization in the
    \nWatson IoT Platform.\n\nPlease note the the delete will fail if the thing being
    deleted is \ncurrently being aggregated by other thing instances."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//thing/types/{thingTypeId}/things/{thingId}
  tags: Internet of Things,Thing,Types,ThingTypeId,Things,ThingId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/thingtypesthingtypeidthingsthingid-delete-openapi.md
- name: IBM Watson IoT Platform Get the state for the thing with the specified id
  x-api-slug: ibm-watson-iot-platform
  description: Retrieve the current state of the thing with the specified id.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//thing/types/{thingTypeId}/things/{thingId}/state/{logicalInterfaceId}
  tags: Internet of Things,Thing,Types,ThingTypeId,Things,ThingId,State,LogicalInterfaceId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/thingtypesthingtypeidthingsthingidstatelogicalinterfaceid-get-openapi.md
- name: IBM Watson IoT Platform Perform an operation against the thing state for a
    logical interface
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Performs the specified operation against the thing state for a logical
    interface. The following values can be specified for the operation
    property:

      - reset-state

    The **reset-state** operation will reset the state of the specified
    thing instance to the default values as defined by the schema for the
    logical interface.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//thing/types/{thingTypeId}/things/{thingId}/state/{logicalInterfaceId}
  tags: Internet of Things,Thing,Types,ThingTypeId,Things,ThingId,State,LogicalInterfaceId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/thingtypesthingtypeidthingsthingidstatelogicalinterfaceid-patch-openapi.md
- name: IBM Watson IoT Platform
  x-api-slug: ibm-watson-iot-platform
  description: Meet IBM Watson, a cognitive system that enables a new partnership
    between people and computers that enhances and scales human expertise. Watson
    has been learning the language of professions and is trained by experts to work
    across many different industries.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002
  tags: IBM Watson
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/openapi.md
- name: IBM Watson Machine Learning Get Entity Token
  x-api-slug: ibm-watson-machine-learning
  description: Tokens are required for the ML REST API authentication. They are generated
    using ML service credentials
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https://ibm-watson-ml.mybluemix.net/v3///identity/token
  tags: Machine Learning,Identity,Token
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/identitytoken-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/identitytoken-get-openapi.md
- name: IBM Watson Machine Learning Put Entity Token
  x-api-slug: ibm-watson-machine-learning
  description: Refreshes token, accepts expired token and generates a new one (if
    the application binding / service key is still valid)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https://ibm-watson-ml.mybluemix.net/v3///identity/token
  tags: Machine Learning,Identity,Token
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/identitytoken-put-openapi.md
- name: IBM Watson Machine Learning Get Wml Instances Instance Published Models
  x-api-slug: ibm-watson-machine-learning
  description: Get wml instances instance published models.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https://ibm-watson-ml.mybluemix.net/v3///wml_instances/{instance_id}/published_models
  tags: Machine Learning,Wml,Instances,Instance,Id,Published,Models
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/wml-instancesinstance-idpublished-models-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/wml-instancesinstance-idpublished-models-get-openapi.md
- name: IBM Watson Machine Learning Get Wml Instances Instance Published Models Published
    Model
  x-api-slug: ibm-watson-machine-learning
  description: Get wml instances instance published models published model.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https://ibm-watson-ml.mybluemix.net/v3///wml_instances/{instance_id}/published_models/{published_model_id}
  tags: Machine Learning,Wml,Instances,Instance,Id,Published,Models,Published,Model,Id
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/wml-instancesinstance-idpublished-modelspublished-model-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/wml-instancesinstance-idpublished-modelspublished-model-id-get-openapi.md
- name: IBM Watson Machine Learning Delete Wml Instances Instance Published Models
    Published Model
  x-api-slug: ibm-watson-machine-learning
  description: Delete wml instances instance published models published model.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https://ibm-watson-ml.mybluemix.net/v3///wml_instances/{instance_id}/published_models/{published_model_id}
  tags: Machine Learning,Wml,Instances,Instance,Id,Published,Models,Published,Model,Id
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/wml-instancesinstance-idpublished-modelspublished-model-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/wml-instancesinstance-idpublished-modelspublished-model-id-delete-openapi.md
- name: IBM Watson Machine Learning Patch Wml Instances Instance Published Models
    Published Model
  x-api-slug: ibm-watson-machine-learning
  description: Patch wml instances instance published models published model.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https://ibm-watson-ml.mybluemix.net/v3///wml_instances/{instance_id}/published_models/{published_model_id}
  tags: Machine Learning,Wml,Instances,Instance,Id,Published,Models,Published,Model,Id
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/wml-instancesinstance-idpublished-modelspublished-model-id-patch-openapi.md
- name: IBM Watson Machine Learning Get Wml Instances Instance Published Models Published
    Model Evaluation Metrics
  x-api-slug: ibm-watson-machine-learning
  description: Get wml instances instance published models published model evaluation
    metrics.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https://ibm-watson-ml.mybluemix.net/v3///wml_instances/{instance_id}/published_models/{published_model_id}/evaluation_metrics
  tags: Machine Learning,Wml,Instances,Instance,Id,Published,Models,Published,Model,Id,Evaluation,Metrics
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/wml-instancesinstance-idpublished-modelspublished-model-idevaluation-metrics-get-openapi.md
- name: IBM Watson Machine Learning Put Wml Instances Instance Published Models Published
    Model Learning Configuration
  x-api-slug: ibm-watson-machine-learning
  description: Put wml instances instance published models published model learning
    configuration.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https://ibm-watson-ml.mybluemix.net/v3///wml_instances/{instance_id}/published_models/{published_model_id}/learning_configuration
  tags: Machine Learning,Wml,Instances,Instance,Id,Published,Models,Published,Model,Id,Learning,Configuration
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/wml-instancesinstance-idpublished-modelspublished-model-idlearning-configuration-put-openapi.md
- name: IBM Watson Machine Learning Patch Wml Instances Instance Published Models
    Published Model Learning Configuration
  x-api-slug: ibm-watson-machine-learning
  description: Patch wml instances instance published models published model learning
    configuration.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https://ibm-watson-ml.mybluemix.net/v3///wml_instances/{instance_id}/published_models/{published_model_id}/learning_configuration
  tags: Machine Learning,Wml,Instances,Instance,Id,Published,Models,Published,Model,Id,Learning,Configuration
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/wml-instancesinstance-idpublished-modelspublished-model-idlearning-configuration-patch-openapi.md
- name: IBM Watson Machine Learning Post Wml Instances Instance Published Models Published
    Model Learning Iterations
  x-api-slug: ibm-watson-machine-learning
  description: Post wml instances instance published models published model learning
    iterations.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https://ibm-watson-ml.mybluemix.net/v3///wml_instances/{instance_id}/published_models/{published_model_id}/learning_iterations
  tags: Machine Learning,Wml,Instances,Instance,Id,Published,Models,Published,Model,Id,Learning,Iterations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/wml-instancesinstance-idpublished-modelspublished-model-idlearning-iterations-post-openapi.md
- name: IBM Watson Machine Learning Get Wml Instances Instance Published Models Published
    Model Learning Iterations
  x-api-slug: ibm-watson-machine-learning
  description: Get wml instances instance published models published model learning
    iterations.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https://ibm-watson-ml.mybluemix.net/v3///wml_instances/{instance_id}/published_models/{published_model_id}/learning_iterations
  tags: Machine Learning,Wml,Instances,Instance,Id,Published,Models,Published,Model,Id,Learning,Iterations
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/wml-instancesinstance-idpublished-modelspublished-model-idlearning-iterations-get-openapi.md
- name: IBM Watson Machine Learning Get Wml Instances Instance Published Models Published
    Model Learning Iterations Learning Iteration
  x-api-slug: ibm-watson-machine-learning
  description: Get wml instances instance published models published model learning
    iterations learning iteration.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https://ibm-watson-ml.mybluemix.net/v3///wml_instances/{instance_id}/published_models/{published_model_id}/learning_iterations/{learning_iteration_id}
  tags: Machine Learning,Wml,Instances,Instance,Id,Published,Models,Published,Model,Id,Learning,Iterations,Learning,Iteration,Id
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/wml-instancesinstance-idpublished-modelspublished-model-idlearning-iterationslearning-iteration-id-get-openapi.md
- name: IBM Watson Machine Learning Post Wml Instances Instance Published Models Published
    Model Feedback
  x-api-slug: ibm-watson-machine-learning
  description: |-
    Receives the feedback data and stores it in the feedback store
    defined in learning configuration
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https://ibm-watson-ml.mybluemix.net/v3///wml_instances/{instance_id}/published_models/{published_model_id}/feedback
  tags: Machine Learning,Wml,Instances,Instance,Id,Published,Models,Published,Model,Id,Feedback
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/wml-instancesinstance-idpublished-modelspublished-model-idfeedback-post-openapi.md
- name: IBM Watson Machine Learning Post Wml Instances Instance Published Models Published
    Model Deployments
  x-api-slug: ibm-watson-machine-learning
  description: Creates the deployment - online, stream, batch (batch deployment only
    supports Cloud Object Storage as input/output for Tensorflow, Keras and Caffe
    models.)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https://ibm-watson-ml.mybluemix.net/v3///wml_instances/{instance_id}/published_models/{published_model_id}/deployments
  tags: Machine Learning,Wml,Instances,Instance,Id,Published,Models,Published,Model,Id,Deployments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/wml-instancesinstance-idpublished-modelspublished-model-iddeployments-post-openapi.md
- name: IBM Watson Machine Learning Get Wml Instances Instance Published Models Published
    Model Deployments
  x-api-slug: ibm-watson-machine-learning
  description: Get wml instances instance published models published model deployments.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https://ibm-watson-ml.mybluemix.net/v3///wml_instances/{instance_id}/published_models/{published_model_id}/deployments
  tags: Machine Learning,Wml,Instances,Instance,Id,Published,Models,Published,Model,Id,Deployments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/wml-instancesinstance-idpublished-modelspublished-model-iddeployments-get-openapi.md
- name: IBM Watson Machine Learning Get Wml Instances Instance Published Models Published
    Model Deployments Deployment
  x-api-slug: ibm-watson-machine-learning
  description: Get wml instances instance published models published model deployments
    deployment.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https://ibm-watson-ml.mybluemix.net/v3///wml_instances/{instance_id}/published_models/{published_model_id}/deployments/{deployment_id}
  tags: Machine Learning,Wml,Instances,Instance,Id,Published,Models,Published,Model,Id,Deployments,Deployment,Id
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/wml-instancesinstance-idpublished-modelspublished-model-iddeploymentsdeployment-id-get-openapi.md
- name: IBM Watson Machine Learning Patch Wml Instances Instance Published Models
    Published Model Deployments Deployment
  x-api-slug: ibm-watson-machine-learning
  description: Patch wml instances instance published models published model deployments
    deployment.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https://ibm-watson-ml.mybluemix.net/v3///wml_instances/{instance_id}/published_models/{published_model_id}/deployments/{deployment_id}
  tags: Machine Learning,Wml,Instances,Instance,Id,Published,Models,Published,Model,Id,Deployments,Deployment,Id
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/wml-instancesinstance-idpublished-modelspublished-model-iddeploymentsdeployment-id-patch-openapi.md
- name: IBM Watson Machine Learning Delete Wml Instances Instance Published Models
    Published Model Deployments Deployment
  x-api-slug: ibm-watson-machine-learning
  description: Delete wml instances instance published models published model deployments
    deployment.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https://ibm-watson-ml.mybluemix.net/v3///wml_instances/{instance_id}/published_models/{published_model_id}/deployments/{deployment_id}
  tags: Machine Learning,Wml,Instances,Instance,Id,Published,Models,Published,Model,Id,Deployments,Deployment,Id
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/wml-instancesinstance-idpublished-modelspublished-model-iddeploymentsdeployment-id-delete-openapi.md
- name: IBM Watson Machine Learning Post Wml Instances Instance Published Models Published
    Model Deployments Deployment Online
  x-api-slug: ibm-watson-machine-learning
  description: Post wml instances instance published models published model deployments
    deployment online.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https://ibm-watson-ml.mybluemix.net/v3///wml_instances/{instance_id}/published_models/{published_model_id}/deployments/{deployment_id}/online
  tags: Machine Learning,Wml,Instances,Instance,Id,Published,Models,Published,Model,Id,Deployments,Deployment,Id,Online
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/wml-instancesinstance-idpublished-modelspublished-model-iddeploymentsdeployment-idonline-post-openapi.md
- name: IBM Watson Machine Learning Get Wml Instances Instance Deployments
  x-api-slug: ibm-watson-machine-learning
  description: Get wml instances instance deployments.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https://ibm-watson-ml.mybluemix.net/v3///wml_instances/{instance_id}/deployments
  tags: Machine Learning,Wml,Instances,Instance,Id,Deployments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/wml-instancesinstance-iddeployments-get-openapi.md
- name: IBM Watson Machine Learning Get Wml Instances Instance
  x-api-slug: ibm-watson-machine-learning
  description: Details about specific service instance
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https://ibm-watson-ml.mybluemix.net/v3///wml_instances/{instance_id}
  tags: Machine Learning,Wml,Instances,Instance,Id
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/wml-instancesinstance-id-get-openapi.md
- name: IBM Watson Machine Learning
  x-api-slug: ibm-watson-machine-learning
  description: Meet IBM Watson, a cognitive system that enables a new partnership
    between people and computers that enhances and scales human expertise. Watson
    has been learning the language of professions and is trained by experts to work
    across many different industries.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https://ibm-watson-ml.mybluemix.net/v3/
  tags: IBM Watson
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/ibm-watson/master/_listings/ibm-watson/openapi.md
x-common:
- type: x-application-gallery
  url: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/gallery.html
- type: x-blog
  url: https://developer.ibm.com/watson/blog/
- type: x-blog-rss
  url: https://developer.ibm.com/watson/feed/
- type: x-developer
  url: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/doc/
- type: x-developer
  url: https://developer.ibm.com/watson/
- type: x-documentation
  url: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/apis/
- type: x-forum
  url: https://developer.ibm.com/answers/smartspace/watson/
- type: x-getting-started
  url: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/getstarted.html
- type: x-github
  url: https://github.com/IBM-Watson
- type: x-partners
  url: http://www.ibm.com/smarterplanet/us/en/ibmwatson/ecosystem.html
- type: x-privacy
  url: http://www.ibm.com/privacy/us/en/?lnk=flg-priv-usen
- type: x-terms-of-service
  url: http://www.ibm.com/legal/us/en/?lnk=flg-tous-usen
- type: x-twitter
  url: https://twitter.com/IBMWatson
- type: x-videos
  url: http://www.ibm.com/smarterplanet/us/en/ibmwatson/
- type: x-website
  url: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
- type: x-white-papers
  url: https://developer.ibm.com/watson/docs/whitepapers/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---