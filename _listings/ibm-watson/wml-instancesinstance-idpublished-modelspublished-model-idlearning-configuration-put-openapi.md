---
swagger: "2.0"
x-collection-name: IBM Watson
x-complete: 0
info:
  title: IBM Watson Machine Learning Put Wml Instances Instance Published Models Published
    Model Learning Configuration
  description: Put wml instances instance published models published model learning
    configuration.
  version: 1.0.0
basePath: v3/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /schemas:
    get:
      summary: Query active schema definitions
      description: "Schemas are used to define the structure of Events, Device State
        and\nThing State in the Watson IoT Platform.\n\n  - For Events, they define
        the structure of the payload of the events\n    that are published to the
        platform by devices.\n\n  - For Device and Thing State, they define the structure
        of the state\n    that is stored by the platform.\n\nThe **schemas** endpoint
        returns the list of all of the active schema \ndefinitions for the organization
        in the Watson IoT Platform.  Various\nquery parameters can be used to filter,
        sort and page through the list\nof schemas that are returned."
      operationId: schemas-are-used-to-define-the-structure-of-events-device-state-andthing-state-in-the-watson-iot-pla
      x-api-path-slug: schemas-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Schemas
  /schemas/{schemaId}:
    get:
      summary: Get active schema definition metadata
      description: |-
        Retrieves the metadata for the active schema definition with the
        specified id.
      operationId: retrieves-the-metadata-for-the-active-schema-definition-with-thespecified-id
      x-api-path-slug: schemasschemaid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Schemas
      - SchemaId
  /schemas/{schemaId}/content:
    get:
      summary: Get the contents of the active schema definition file
      description: |-
        Retrieves the content of the active schema definition file with the
        specified id.
      operationId: retrieves-the-content-of-the-active-schema-definition-file-with-thespecified-id
      x-api-path-slug: schemasschemaidcontent-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Schemas
      - SchemaId
      - Content
  /draft/schemas:
    get:
      summary: Query draft schema definitions
      description: "Schemas are used to define the structure of Events, Device State
        and\nThing State in the Watson IoT Platform.\n\n  - For Events, they define
        the structure of the payload of the events\n    that are published to the
        platform by devices.\n\n  - For Device and Thing State, they define the structure
        of the state\n    that is stored by the platform.\n\nThe **/draft/schemas**
        endpoint returns the list of all of the draft \nschema for the organization
        in the Watson IoT Platform.  Various query\nparameters can be used to filter,
        sort and page through the list of\nschemas that are returned."
      operationId: schemas-are-used-to-define-the-structure-of-events-device-state-andthing-state-in-the-watson-iot-pla
      x-api-path-slug: draftschemas-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Schemas
    post:
      summary: Create a draft schema definition
      description: "Creates a new draft schema definition for the organization in
        the Watson\nIoT Platform.\n\nThe schema definition file is passed to the Watson
        IoT Platform within a\nmultipart POST (multipart/form-data).  The body of
        the POST **must**\ncontain at least two parts:\n\n  - One with a name of **schemaFile**
        that contains the actual content\n    of the file as the body of the part.\n
        \   \n  - One with a name of **name** that contains a string that defines
        the\n    name of the schema resource in the body of the part.\n\nAdditional
        metadata can be passed in other parts within the multipart\nPOST.  For example,
        to specify a description for the new schema\ndefinition, you should include
        a part with the name **description** and\nthe description as the body of the
        part.  To specify the type of the\nschema, you should include a part with
        the name **schemaType** and one\nof the following in the body of the part
        (the schemaType defaults to\njson-schema if the no schemaType part is present):\n\n
        \ - json-schema\n\nIf parts with names other than those specified above are
        included in the\nmultipart POST the request will fail and an HTTP status code
        of 400 will\nbe returned.\n\nThe content of the schema definition file that
        is passed to the platform\nis stored and a REST resource is created containing
        metadata that\ndescribes the schema definition."
      operationId: creates-a-new-draft-schema-definition-for-the-organization-in-the-watsoniot-platformthe-schema-defin
      x-api-path-slug: draftschemas-post
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Schemas
  /draft/schemas/{schemaId}:
    get:
      summary: Get draft schema definition metadata
      description: |-
        Retrieves the metadata for the draft schema definition with the
        specified id.
      operationId: retrieves-the-metadata-for-the-draft-schema-definition-with-thespecified-id
      x-api-path-slug: draftschemasschemaid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Schemas
      - SchemaId
    put:
      summary: Update draft schema definition metadata
      description: "Updates the metadata for the draft schema definition with the
        specified\nid. The following properties can be updated:\n\n  - name\n  - description\n
        \ \nNote that if the description field is omitted from the body of the\nupdate,
        then any existing description will be removed from the schema\ndefinition.\n
        \ \nAny changes made to the values of the following properties will be\nignored:\n\n
        \ - schemaType\n  - schemaFilename\n  - contentType\n  - created\n  - createdBy\n
        \ - updated\n  - updatedBy\n  - refs\n  \nThe schemaFilename and contentType
        properties are updated when the\ncontent of the schema file is updated.\n\nThe
        values of the created, createdBy, updated, updatedBy and refs\nproperties
        are set on the server as a result of a successful update."
      operationId: updates-the-metadata-for-the-draft-schema-definition-with-the-specifiedid-the-following-properties-c
      x-api-path-slug: draftschemasschemaid-put
      parameters:
      - in: query
        name: No Name
      - in: body
        name: schemaDefinition
        description: The JSON representation of the schema definition
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Schemas
      - SchemaId
    delete:
      summary: Delete a draft schema definition
      description: |-
        Deletes the draft schema definition with the specified id from the
        organization in the Watson IoT Platform.  Deleting the schema definition
        deletes both the metadata and the actual schema definition file from the
        Watson IoT Platform.

        Please note the the delete will fail if the draft schema definition is
        being referenced by an event type or logical interface.
      operationId: deletes-the-draft-schema-definition-with-the-specified-id-from-theorganization-in-the-watson-iot-pla
      x-api-path-slug: draftschemasschemaid-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Schemas
      - SchemaId
  /draft/schemas/{schemaId}/content:
    get:
      summary: Get the contents of the draft schema definition file
      description: |-
        Retrieves the content of the draft schema definition file with the
        specified id.
      operationId: retrieves-the-content-of-the-draft-schema-definition-file-with-thespecified-id
      x-api-path-slug: draftschemasschemaidcontent-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Schemas
      - SchemaId
      - Content
    put:
      summary: Update the content of a draft schema definition file
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
      operationId: updates-the-content-of-a-draft-schema-definition-file-with-the-specifiedidthe-schema-definition-file
      x-api-path-slug: draftschemasschemaidcontent-put
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Schemas
      - SchemaId
      - Content
  /event/types:
    get:
      summary: Query active event types
      description: |-
        Event types are used to model the events that are published to the
        Watson IoT Platform.  An event type must be created in an organization
        before more complex processing can be performed on the native event.

        The **/event/types** endpoint returns the list of all of the active
        event types that have been defined for the organization in the Watson
        IoT Platform.  Various query parameters can be used to filter, sort and
        page through the list of active event types that are returned.
      operationId: event-types-are-used-to-model-the-events-that-are-published-to-thewatson-iot-platform--an-event-type
      x-api-path-slug: eventtypes-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Event
      - Types
  /event/types/{eventTypeId}:
    get:
      summary: Get an active event type
      description: Retrieve the active event type with the specified id.
      operationId: retrieve-the-active-event-type-with-the-specified-id
      x-api-path-slug: eventtypeseventtypeid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Event
      - Types
      - EventTypeId
  /draft/event/types:
    get:
      summary: Query draft event types
      description: |-
        Event types are used to model the events that are published to the
        Watson IoT Platform.  An event type must be created in an organization
        before more complex processing can be performed on the native event.

        The **/draft/event/types** endpoint returns the list of all of the draft
        event types that have been defined for the organization in the Watson
        IoT Platform.  Various query parameters can be used to filter, sort and
        page through the list of draft event types that are returned.
      operationId: event-types-are-used-to-model-the-events-that-are-published-to-thewatson-iot-platform--an-event-type
      x-api-path-slug: drafteventtypes-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Event
      - Types
    post:
      summary: Create a draft event type
      description: |-
        Creates a new draft event type for the organization in the Watson IoT
        Platform.  The draft event type must reference the schema definition
        that defines the structure of the inbound MQTT event.
      operationId: creates-a-new-draft-event-type-for-the-organization-in-the-watson-iotplatform--the-draft-event-type-
      x-api-path-slug: drafteventtypes-post
      parameters:
      - in: body
        name: Event Type
        description: The JSON representation of the draft event type
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Event
      - Types
  /draft/event/types/{eventTypeId}:
    get:
      summary: Get a draft event type
      description: Retrieve the draft event type with the specified id.
      operationId: retrieve-the-draft-event-type-with-the-specified-id
      x-api-path-slug: drafteventtypeseventtypeid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Event
      - Types
      - EventTypeId
    put:
      summary: Update a draft event type
      description: "Updates the draft event type with the specified id. The following\nproperties
        can be updated:\n\n  - name\n  - description\n  - schemaId\n\nNote that if
        the description field is omitted from the body of the\nupdate, then any existing
        description will be removed from the event\ntype.\n  \nAny changes made to
        the values of the following properties will be\nignored:\n\n  - created\n
        \ - createdBy\n  - updated\n  - updatedBy\n  - refs\n  \nThe values of these
        properties are set on the server as a result of a\nsuccessful update."
      operationId: updates-the-draft-event-type-with-the-specified-id-the-followingproperties-can-be-updated---name---d
      x-api-path-slug: drafteventtypeseventtypeid-put
      parameters:
      - in: body
        name: Event Type
        description: The JSON representation of the event type
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Event
      - Types
      - EventTypeId
    delete:
      summary: Delete a draft event type
      description: "Deletes the draft event type with the specified id from the organization\nin
        the Watson IoT Platform.\n\nPlease note the the delete will fail if the draft
        event type is being \nreferenced by a physical interface."
      operationId: deletes-the-draft-event-type-with-the-specified-id-from-the-organizationin-the-watson-iot-platformpl
      x-api-path-slug: drafteventtypeseventtypeid-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Event
      - Types
      - EventTypeId
  /physicalinterfaces:
    get:
      summary: Query active phyiscal interfaces
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
      operationId: physical-interfaces-are-used-to-model-the-interfaces-between-physicaldevices-and-the-watson-iot-plat
      x-api-path-slug: physicalinterfaces-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Physicalinterfaces
  /physicalinterfaces/{physicalInterfaceId}:
    get:
      summary: Get an active physical interface
      description: Retrieve the active physical interface with the specified id.
      operationId: retrieve-the-active-physical-interface-with-the-specified-id
      x-api-path-slug: physicalinterfacesphysicalinterfaceid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Physicalinterfaces
      - PhysicalInterfaceId
  /physicalinterfaces/{physicalInterfaceId}/events:
    get:
      summary: Get the list of event mappings
      description: |-
        Retrieve the list of event mappings for the active physical interface.
        Event mappings are keyed off of the event id specified in the MQTT topic
        that the inbound events are published to.
      operationId: retrieve-the-list-of-event-mappings-for-the-active-physical-interfaceevent-mappings-are-keyed-off-of
      x-api-path-slug: physicalinterfacesphysicalinterfaceidevents-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Physicalinterfaces
      - PhysicalInterfaceId
      - Events
  /draft/physicalinterfaces:
    get:
      summary: Query draft phyiscal interfaces
      description: "Physical interfaces are used to model the interfaces between physical\ndevices
        and the Watson IoT Platform.  A physical interface references\nevent types.
        \ Devices that implement a physical interface publish these\nevents to the
        platform.\n\nThe event types are referenced via a mapping that maps an event
        id to\nthe id of an event type.  The event id corresponds to the MQTT topic\nthat
        the event is published to by a device.\n\nThe **/draft/physicalinterfaces**
        endpoint returns the list of all of \nthe draft physical interfaces that have
        been defined for the\norganization in the Watson IoT Platform.  Various query
        parameters can\nbe used to filter, sort and page through the list of draft
        physical\ninterfaces that are returned."
      operationId: physical-interfaces-are-used-to-model-the-interfaces-between-physicaldevices-and-the-watson-iot-plat
      x-api-path-slug: draftphysicalinterfaces-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Physicalinterfaces
    post:
      summary: Create a draft physical interface
      description: "Creates a new draft physical interface for the organization in
        the \nWatson IoT Platform."
      operationId: creates-a-new-draft-physical-interface-for-the-organization-in-the-watson-iot-platform
      x-api-path-slug: draftphysicalinterfaces-post
      parameters:
      - in: body
        name: Physical Interface
        description: The JSON representation of the physical interface
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Physicalinterfaces
  /draft/physicalinterfaces/{physicalInterfaceId}:
    get:
      summary: Get a draft physical interface
      description: Retrieve the draft physical interface with the specified id.
      operationId: retrieve-the-draft-physical-interface-with-the-specified-id
      x-api-path-slug: draftphysicalinterfacesphysicalinterfaceid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Physicalinterfaces
      - PhysicalInterfaceId
    put:
      summary: Update a draft physical interface
      description: "Updates the draft physical interface with the specified id. The
        \nfollowing properties can be updated:\n\n  - name\n  - description\n\nNote
        that if the description field is omitted from the body of the\nupdate, then
        any existing description will be removed from the physical\ninterface.\n  \nAny
        changes made to the values of the following properties will be\nignored:\n\n
        \ - created\n  - createdBy\n  - updated\n  - updatedBy\n  - refs\n  \nThe
        values of these properties are set on the server as a result of a\nsuccessful
        update."
      operationId: updates-the-draft-physical-interface-with-the-specified-id-the-following-properties-can-be-updated--
      x-api-path-slug: draftphysicalinterfacesphysicalinterfaceid-put
      parameters:
      - in: query
        name: No Name
      - in: body
        name: Physical Interface
        description: The JSON representation of the physical interface
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Physicalinterfaces
      - PhysicalInterfaceId
    delete:
      summary: Delete a draft physical interface
      description: |-
        Deletes the draft physical interface with the specified id from the
        organization in the Watson IoT Platform.

        Please note the the delete will fail if the draft physical interface is
        being referenced  by a device type.
      operationId: deletes-the-draft-physical-interface-with-the-specified-id-from-theorganization-in-the-watson-iot-pl
      x-api-path-slug: draftphysicalinterfacesphysicalinterfaceid-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Physicalinterfaces
      - PhysicalInterfaceId
  /draft/physicalinterfaces/{physicalInterfaceId}/events:
    get:
      summary: Get the list of event mappings
      description: |-
        Retrieve the list of event mappings for the draft physical interface.
        Event mappings are keyed off of the event id specified in the MQTT topic
        that the inbound events are published to.
      operationId: retrieve-the-list-of-event-mappings-for-the-draft-physical-interfaceevent-mappings-are-keyed-off-of-
      x-api-path-slug: draftphysicalinterfacesphysicalinterfaceidevents-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Physicalinterfaces
      - PhysicalInterfaceId
      - Events
    post:
      summary: Map an event to the draft physical interface
      description: |-
        Maps an event id to a specific event type for the draft specified
        physical interface.
      operationId: maps-an-event-id-to-a-specific-event-type-for-the-draft-specifiedphysical-interface
      x-api-path-slug: draftphysicalinterfacesphysicalinterfaceidevents-post
      parameters:
      - in: body
        name: Event Mapping
        description: The JSON representation of the event mapping
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Physicalinterfaces
      - PhysicalInterfaceId
      - Events
  /draft/physicalinterfaces/{physicalInterfaceId}/events/{eventId}:
    delete:
      summary: Remove an event mapping from the draft physical interface
      description: |-
        Removes the event mapping with the specified id from the draft physical
        interface.
      operationId: removes-the-event-mapping-with-the-specified-id-from-the-draft-physicalinterface
      x-api-path-slug: draftphysicalinterfacesphysicalinterfaceideventseventid-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Physicalinterfaces
      - PhysicalInterfaceId
      - Events
      - EventId
  /logicalinterfaces:
    get:
      summary: Query active logical interfaces
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
      operationId: logical-interfaces-are-used-to-model-the-interfaces-exposed-by-adevice-or-thing-in-the-watson-iot-pl
      x-api-path-slug: logicalinterfaces-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Logical interfaces
  /logicalinterfaces/{logicalInterfaceId}:
    get:
      summary: Get an active logical interface
      description: Retrieve the active logical interface with the specified id.
      operationId: retrieve-the-active-logical-interface-with-the-specified-id
      x-api-path-slug: logicalinterfaceslogicalinterfaceid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Logical interfaces
      - LogicalInterfaceId
    patch:
      summary: Perform an operation against a logical interface
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
      operationId: performs-the-specified-operation-against-the-logical-interface-thefollowing-values-can-be-specified-
      x-api-path-slug: logicalinterfaceslogicalinterfaceid-patch
      parameters:
      - in: query
        name: No Name
      - in: body
        name: Operation
        description: The JSON representation of an operation
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Logical interfaces
      - LogicalInterfaceId
  /draft/logicalinterfaces:
    get:
      summary: Query draft logical interfaces
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
      operationId: logical-interfaces-are-used-to-model-the-interfaces-exposed-by-adevice-or-thing-in-the-watson-iot-pl
      x-api-path-slug: draftlogicalinterfaces-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Logical interfaces
    post:
      summary: Create a draft logical interface
      description: |-
        Creates a new draft logical interface for the organization in the
        Watson IoT Platform. The logical interface must reference a schema
        definition that defines the structure of the state that will be stored
        for the device or thing.
      operationId: creates-a-new-draft-logical-interface-for-the-organization-in-thewatson-iot-platform-the-logical-int
      x-api-path-slug: draftlogicalinterfaces-post
      parameters:
      - in: body
        name: Logical Interface
        description: The JSON representation of the draft logical interface
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Logical interfaces
  /draft/logicalinterfaces/{logicalInterfaceId}:
    get:
      summary: Get a draft logical interface
      description: Retrieve the draft logical interface with the specified id.
      operationId: retrieve-the-draft-logical-interface-with-the-specified-id
      x-api-path-slug: draftlogicalinterfaceslogicalinterfaceid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Logical interfaces
      - LogicalInterfaceId
    put:
      summary: Update a draft logical interface
      description: "Updates the draft logical interface with the specified id. The\nfollowing
        properties can be updated: \n\n  - name\n  - description\n  - schemaId\n\nNote
        that if the description field is omitted from the body of the\nupdate, then
        any existing description will be removed from the logical\ninterface.\n  \nAny
        changes made to the values of the following properties will be\nignored:\n\n
        \ - created\n  - createdBy\n  - updated\n  - updatedBy\n  - refs\n  \nThe
        values of these properties are set on the server as a result of a\nsuccessful
        update."
      operationId: updates-the-draft-logical-interface-with-the-specified-id-thefollowing-properties-can-be-updated----
      x-api-path-slug: draftlogicalinterfaceslogicalinterfaceid-put
      parameters:
      - in: body
        name: Logical Interface
        description: The JSON representation of the draft logical interface
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Logical interfaces
      - LogicalInterfaceId
    patch:
      summary: Perform an operation against a draft logical interface
      description: "Performs the specified operation against the draft logical\ninterface.
        The following values can be specified for the operation\nproperty:\n\n  -
        validate-configuration\n  - activate-configuration\n  - list-differences\n\nThe
        **validate-configuration** operation will analyze all of the \nconfiguration
        associated with the draft logical interface to\ndetermine if it is valid.
        \ If the configuration is invalid, a list of \nthe issues will be returned
        in the body of the response.  \n \nThe **activate-configuration** operation
        will make the configuration\nassociated with the draft logical interface active.
        The \n**activate-configuration** operation must have been performed against\na
        draft logical interface before any state is generated for device\nor thing
        types that are associated with that logical interface.\n\nThe **list-differences**
        operation will return a list of the differences\nthat exist between the active
        configuration for the logical\ninterface, if any, and the draft configuration."
      operationId: performs-the-specified-operation-against-the-draft-logicalinterface-the-following-values-can-be-spec
      x-api-path-slug: draftlogicalinterfaceslogicalinterfaceid-patch
      parameters:
      - in: query
        name: No Name
      - in: body
        name: Operation
        description: The JSON representation of the operation
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Logical interfaces
      - LogicalInterfaceId
    delete:
      summary: Delete a draft logical interface
      description: |-
        Deletes the draft logical interface with the specified id from the
        organization in the Watson IoT Platform.

        Please note the the delete will fail if the draft logical interface
        is being referenced by a device type.
      operationId: deletes-the-draft-logical-interface-with-the-specified-id-from-theorganization-in-the-watson-iot-pla
      x-api-path-slug: draftlogicalinterfaceslogicalinterfaceid-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Logical interfaces
      - LogicalInterfaceId
  /logicalinterfaces/{logicalInterfaceId}/rules:
    get:
      summary: Query active rules
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
      operationId: rules-allow-you-to-specify-conditions-that-can-be-used-to-triggeractions-for-example-you-might-creat
      x-api-path-slug: logicalinterfaceslogicalinterfaceidrules-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Logical interfaces
      - LogicalInterfaceId
      - Rules
  /logicalinterfaces/{logicalInterfaceId}/rules/{ruleId}:
    get:
      summary: Get an active rule
      description: |-
        Retrieve the active rule with the specified id that has been associated
        with the specified logical interface.
      operationId: retrieve-the-active-rule-with-the-specified-id-that-has-been-associatedwith-the-specified-logical-in
      x-api-path-slug: logicalinterfaceslogicalinterfaceidrulesruleid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Logical interfaces
      - LogicalInterfaceId
      - Rules
      - RuleId
  /draft/logicalinterfaces/{logicalInterfaceId}/rules:
    get:
      summary: Query draft rules
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
      operationId: rules-allow-you-to-specify-conditions-that-can-be-used-to-triggeractions-for-example-you-might-creat
      x-api-path-slug: draftlogicalinterfaceslogicalinterfaceidrules-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Logical interfaces
      - LogicalInterfaceId
      - Rules
    post:
      summary: Create a draft rule
      description: |-
        Creates a new draft rule that is associated with the logical interface
        for the organization in the Watson IoT Platform.
      operationId: creates-a-new-draft-rule-that-is-associated-with-the-logical-interfacefor-the-organization-in-the-wa
      x-api-path-slug: draftlogicalinterfaceslogicalinterfaceidrules-post
      parameters:
      - in: query
        name: No Name
      - in: body
        name: Rule
        description: The JSON representation of the draft rule
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Logical interfaces
      - LogicalInterfaceId
      - Rules
  /draft/logicalinterfaces/{logicalInterfaceId}/rules/{ruleId}:
    get:
      summary: Get a draft rule
      description: |-
        Retrieve the draft rule with the specified id that has been associated
        with the specified logical interface.
      operationId: retrieve-the-draft-rule-with-the-specified-id-that-has-been-associatedwith-the-specified-logical-int
      x-api-path-slug: draftlogicalinterfaceslogicalinterfaceidrulesruleid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Logical interfaces
      - LogicalInterfaceId
      - Rules
      - RuleId
    put:
      summary: Update a draft rule
      description: "Updates the draft rule with the specified id. The following properties\ncan
        be updated: \n\n  - name\n  - description\n  - condition\n\nNote that if the
        description field is omitted from the body of the\nupdate, then any existing
        description will be removed from the rule.\n  \nAny changes made to the values
        of the following properties will be\nignored:\n\n  - created\n  - createdBy\n
        \ - updated\n  - updatedBy\n  - refs\n  \nThe values of these properties are
        set on the server as a result of a\nsuccessful update."
      operationId: updates-the-draft-rule-with-the-specified-id-the-following-propertiescan-be-updated----name---descri
      x-api-path-slug: draftlogicalinterfaceslogicalinterfaceidrulesruleid-put
      parameters:
      - in: query
        name: No Name
      - in: body
        name: Rule
        description: The JSON representation of the draft rule
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Logical interfaces
      - LogicalInterfaceId
      - Rules
      - RuleId
    delete:
      summary: Delete a draft rule
      description: |-
        Deletes the draft rule with the specified id from the organization in
        the Watson IoT Platform.
      operationId: deletes-the-draft-rule-with-the-specified-id-from-the-organization-inthe-watson-iot-platform
      x-api-path-slug: draftlogicalinterfaceslogicalinterfaceidrulesruleid-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Logical interfaces
      - LogicalInterfaceId
      - Rules
      - RuleId
  /device/types:
    get:
      summary: List device types
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
      operationId: sorting-can-be-performed-on-any-of-the-following-properties-sortorder-can-be-reversed-by-prefixing-t
      x-api-path-slug: devicetypes-get
      parameters:
      - in: query
        name: description
        description: Optional filter of results by description
      - in: query
        name: id
        description: Optional filter of results by ID
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Device
      - Types
  /device/types/{typeId}:
    patch:
      summary: Perform an operation against a device type
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
      operationId: performs-the-specified-operation-against-the-device-type-the-followingvalues-can-be-specified-for-th
      x-api-path-slug: devicetypestypeid-patch
      parameters:
      - in: body
        name: Device Type Operation
        description: The JSON representation of a device type operation
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Device
      - Types
  /device/types/{typeId}/physicalinterface:
    get:
      summary: Get the active physical interface associated with the device type
      description: |-
        Retrieve the active physical interface that has been associated with the
        device type.  At least one active physical interface must be associated
        with the device type before any mappings can be defined that will
        generate state for the device.
      operationId: retrieve-the-active-physical-interface-that-has-been-associated-with-thedevice-type--at-least-one-ac
      x-api-path-slug: devicetypestypeidphysicalinterface-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Device
      - Types
      - Physicalinterface
  /device/types/{typeId}/logicalinterfaces:
    get:
      summary: |-
        Get the list of active logical interfaces associated with the device
        type
      description: |-
        Retrieve the list of active logical interfaces that have been
        associated with the device type.  At least one logical interface
        must be associated with the device type before any mappings can be
        defined that will generate state for the device.
      operationId: retrieve-the-list-of-active-logical-interfaces-that-have-beenassociated-with-the-device-type--at-lea
      x-api-path-slug: devicetypestypeidlogicalinterfaces-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Device
      - Types
      - Logical interfaces
  /device/types/{typeId}/mappings:
    get:
      summary: Get the list of active property mappings for the device type
      description: |-
        Retrieve the list of active property mappings for the specified device
        type.  A property mapping defines how properties from inbound events are
        mapped to properties defined on an logical interface associated with
        the device type.
      operationId: retrieve-the-list-of-active-property-mappings-for-the-specified-devicetype--a-property-mapping-defin
      x-api-path-slug: devicetypestypeidmappings-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Device
      - Types
      - Mappings
  /device/types/{typeId}/mappings/{logicalInterfaceId}:
    get:
      summary: |-
        Get the active property mappings for a specific logical interface
        for a device type.
      description: |-
        Retrieves the active property mappings for a specific logical
        interface for the device type.
      operationId: retrieves-the-active-property-mappings-for-a-specific-logicalinterface-for-the-device-type
      x-api-path-slug: devicetypestypeidmappingslogicalinterfaceid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Device
      - Types
      - Mappings
      - LogicalInterfaceId
  /draft/device/types:
    get:
      summary: List device types associated with an logical or physical interface
      description: |-
        Retrieves the list of device types that are associated with the
        logical interface and/or physical interface with the ids specified
        using the corresponding query parameters.

        Note that at least one of the following query parameters must be
        specified:

          - logicalInterfaceId
          - physicalInterfaceId
      operationId: retrieves-the-list-of-device-types-that-are-associated-with-thelogical-interface-andor-physical-inte
      x-api-path-slug: draftdevicetypes-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Device
      - Types
  /draft/device/types/{typeId}:
    patch:
      summary: Perform an operation against a draft device type
      description: "Performs the specified operation against the draft device type.
        The\nfollowing values can be specified for the operation property:\n\n  -
        validate-configuration\n  - activate-configuration\n  - list-differences\n\nThe
        **validate-configuration** operation will analyze all of the \nconfiguration
        associated with the draft device type to determine if it\nis valid.  If the
        configuration is invalid, a list of the issues will\nbe returned in the body
        of the response.  \n \nThe **activate-configuration** operation will make
        the configuration\nassociated with the draft device type active. The\n**activate-configuration**
        operation must have been performed against a\ndraft device type before any
        state is generated for instances of that\ntype.\n\nThe **list-differences**
        operation will return a list of the differences\nthat exist between the active
        configuration for the device type, if\nany, and the draft configuration."
      operationId: performs-the-specified-operation-against-the-draft-device-type-thefollowing-values-can-be-specified-
      x-api-path-slug: draftdevicetypestypeid-patch
      parameters:
      - in: body
        name: Device Type Operation
        description: The JSON representation of a device type operation
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Device
      - Types
  /draft/device/types/{typeId}/physicalinterface:
    get:
      summary: Get the draft physical interface associated with the device type
      description: |-
        Retrieve the draft physical interface that has been associated with the
        device type.  At least one active physical interface must be associated
        with the device type before any mappings can be defined that will
        generate state for the device.
      operationId: retrieve-the-draft-physical-interface-that-has-been-associated-with-thedevice-type--at-least-one-act
      x-api-path-slug: draftdevicetypestypeidphysicalinterface-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Device
      - Types
      - Physicalinterface
    post:
      summary: Associate a draft physical interface with the device type
      description: |-
        Associates a draft physical interface with the specified device type.
        The draft physical interface must already exist within the organization
        in the Watson IoT Platform. If a draft physical interface is already
        associated with the device type it will be replaced with the specified
        physical interface.
      operationId: associates-a-draft-physical-interface-with-the-specified-device-typethe-draft-physical-interface-mus
      x-api-path-slug: draftdevicetypestypeidphysicalinterface-post
      parameters:
      - in: query
        name: No Name
      - in: body
        name: Physical Interface
        description: The JSON representation of the draft physical interface
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Device
      - Types
      - Physicalinterface
    delete:
      summary: Disassociate the draft physical interface from the device type
      description: Disassociates the draft physical interface from the device type.
      operationId: disassociates-the-draft-physical-interface-from-the-device-type
      x-api-path-slug: draftdevicetypestypeidphysicalinterface-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Device
      - Types
      - Physicalinterface
  /draft/device/types/{typeId}/logicalinterfaces:
    get:
      summary: |-
        Get the list of draft logical interfaces associated with the device
        type
      description: |-
        Retrieve the list of draft logical interfaces that have been
        associated with the device type.  At least one active logical
        interface must be associated with the device type before any mappings
        can be defined that will generate state for the device.
      operationId: retrieve-the-list-of-draft-logical-interfaces-that-have-beenassociated-with-the-device-type--at-leas
      x-api-path-slug: draftdevicetypestypeidlogicalinterfaces-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Device
      - Types
      - Logical interfaces
    post:
      summary: Associate a draft logical interface with the device type
      description: |-
        Associates a draft logical interface with the specified device type.
        The draft logical interface must already exist within the organization
        in the Watson IoT Platform.
      operationId: associates-a-draft-logical-interface-with-the-specified-device-typethe-draft-logical-interface-must-
      x-api-path-slug: draftdevicetypestypeidlogicalinterfaces-post
      parameters:
      - in: body
        name: Logical Interface
        description: The JSON representation of the draft logical interface
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Device
      - Types
      - Logical interfaces
  /draft/device/types/{typeId}/logicalinterfaces/{logicalInterfaceId}:
    delete:
      summary: Disassociate a draft logical interface from the device type
      description: |-
        Disassociates the draft logical interface  with the specified id
        from the device type.

        Please note the the delete will fail if the draft logical interface
        being removed from the device type is referenced in the property
        mappings for the device type.
      operationId: disassociates-the-draft-logical-interface--with-the-specified-idfrom-the-device-typeplease-note-the-
      x-api-path-slug: draftdevicetypestypeidlogicalinterfaceslogicalinterfaceid-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Device
      - Types
      - Logical interfaces
      - LogicalInterfaceId
  /draft/device/types/{typeId}/mappings:
    get:
      summary: Get the list of draft property mappings for the device type
      description: |-
        Retrieve the list of draft property mappings for the specified device
        type.  A property mapping defines how properties from inbound events are
        mapped to properties defined on an logical interface associated with
        the device type.
      operationId: retrieve-the-list-of-draft-property-mappings-for-the-specified-devicetype--a-property-mapping-define
      x-api-path-slug: draftdevicetypestypeidmappings-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Device
      - Types
      - Mappings
    post:
      summary: |-
        Create the draft property mappings for a logical interface for the
        device type
      description: |-
        Creates the draft property mappings for an logical interface for the
        device type.  The mapping object must specify:
        - The id for for the logical interface that the mappings are for
        - The mappings that define how to map from properties on the inbound
          events to the properties on the logical interface.  The mappings
          are keyed off of the event ids defined by the physical interface
          associated with the device type.
      operationId: creates-the-draft-property-mappings-for-an-logical-interface-for-thedevice-type--the-mapping-object-
      x-api-path-slug: draftdevicetypestypeidmappings-post
      parameters:
      - in: body
        name: Device Type Property Mappings
        description: The JSON representation of the draft device type property mappings
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Device
      - Types
      - Mappings
  /draft/device/types/{typeId}/mappings/{logicalInterfaceId}:
    get:
      summary: |-
        Get the draft property mappings for a specific logical interface for
        a device type.
      description: |-
        Retrieves the draft property mappings for a specific logical
        interface for the device type.
      operationId: retrieves-the-draft-property-mappings-for-a-specific-logicalinterface-for-the-device-type
      x-api-path-slug: draftdevicetypestypeidmappingslogicalinterfaceid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Device
      - Types
      - Mappings
      - LogicalInterfaceId
    put:
      summary: |-
        Update the draft property mappings for a specific logical interface
        for the device type.
      description: |-
        Updates the draft property mappings for a specific logical interface
        for the device type.
      operationId: updates-the-draft-property-mappings-for-a-specific-logical-interfacefor-the-device-type
      x-api-path-slug: draftdevicetypestypeidmappingslogicalinterfaceid-put
      parameters:
      - in: body
        name: Device Type Property Mappings
        description: The JSON representation of the draft device type property mappings
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Device
      - Types
      - Mappings
      - LogicalInterfaceId
    delete:
      summary: |-
        Delete the draft property mappings for a specific logical interface
        for the device type.
      description: |-
        Deletes the draft property mappings for a specific logical interface
        for the device type.
      operationId: deletes-the-draft-property-mappings-for-a-specific-logical-interfacefor-the-device-type
      x-api-path-slug: draftdevicetypestypeidmappingslogicalinterfaceid-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Device
      - Types
      - Mappings
      - LogicalInterfaceId
  /device/types/{typeId}/devices/{deviceId}/state/{logicalInterfaceId}:
    get:
      summary: Get the state for the device with the specified id
      description: Retrieve the current state of the device with the specified id.
      operationId: retrieve-the-current-state-of-the-device-with-the-specified-id
      x-api-path-slug: devicetypestypeiddevicesdeviceidstatelogicalinterfaceid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Device
      - Types
      - Devices
      - DeviceId
      - State
      - LogicalInterfaceId
    patch:
      summary: Perform an operation against the device state for a logical interface
      description: |-
        Performs the specified operation against the device state for a logical
        interface. The following values can be specified for the operation
        property:

          - reset-state

        The **reset-state** operation will reset the state of the specified
        device to the default values as defined by the schema for the logical
        interface.
      operationId: performs-the-specified-operation-against-the-device-state-for-a-logicalinterface-the-following-value
      x-api-path-slug: devicetypestypeiddevicesdeviceidstatelogicalinterfaceid-patch
      parameters:
      - in: query
        name: No Name
      - in: body
        name: Operation
        description: The JSON representation of an operation
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Device
      - Types
      - Devices
      - DeviceId
      - State
      - LogicalInterfaceId
  /thing/types:
    get:
      summary: Query active thing types
      description: "Within the Watson IoT Platform, a Thing allows you to aggregate
        one or\nmore instances of a Device or Thing together to represent a more coarse\ngrained
        object.  For example, you might aggregrate together a temperature\nsensor,
        flow sensor and power sensor together into a Boiler. \n\nThing Types are used
        to model Things.  The Schema associated with a\nThing Type defines the type
        of objects that are aggregated togther to\nmake up an instance of a Thing.
        A Thing Type must be created in an \norganization before in instance of a
        Thing can be created.\n\nThe **/thing/types** endpoint returns the list of
        all of the active\nThing types that have been defined for the organization
        in the Watson IoT\nPlatform. Various query parameters can be used to filter,
        sort and page\nthrough the list of Thing types that are returned."
      operationId: within-the-watson-iot-platform-a-thing-allows-you-to-aggregate-one-ormore-instances-of-a-device-or-t
      x-api-path-slug: thingtypes-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Thing
      - Types
  /thing/types/{thingTypeId}:
    get:
      summary: Get an active thing type
      description: Retrieve the active thing type with the specified id.
      operationId: retrieve-the-active-thing-type-with-the-specified-id
      x-api-path-slug: thingtypesthingtypeid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Thing
      - Types
      - ThingTypeId
    patch:
      summary: Perform an operation against an active thing type
      description: |-
        Performs the specified operation against the active thing type. The
        following values can be specified for the operation property:

          - deactivate-configuration

        The **deactivate-configuration** operation will remove any active
        configuration that is currently associated with the thing type. The
        **deactivate-configuration** operation will fail if there are
        any instances of the thing type.
      operationId: performs-the-specified-operation-against-the-active-thing-type-thefollowing-values-can-be-specified-
      x-api-path-slug: thingtypesthingtypeid-patch
      parameters:
      - in: query
        name: No Name
      - in: body
        name: Thing Type Operation
        description: The JSON representation of a thing type operation
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Thing
      - Types
      - ThingTypeId
  /draft/thing/types:
    get:
      summary: Query draft thing types
      description: "Within the Watson IoT Platform, a Thing allows you to aggregate
        one or\nmore instances of a Device or Thing together to represent a more coarse\ngrained
        object.  For example, you might aggregrate together a temperature\nsensor,
        flow sensor and power sensor together into a Boiler. \n\nThing Types are used
        to model Things.  The Schema associated with a\nThing Type defines the type
        of objects that are aggregated togther to\nmake up an instance of a Thing.
        A Thing Type must be created in an \norganization before in instance of a
        Thing can be created.\n\nThe **/draft/thing/types** endpoint returns the list
        of all of the draft\nThing types that have been defined for the organization
        in the Watson IoT\nPlatform. Various query parameters can be used to filter,
        sort and page\nthrough the list of draft Thing types that are returned."
      operationId: within-the-watson-iot-platform-a-thing-allows-you-to-aggregate-one-ormore-instances-of-a-device-or-t
      x-api-path-slug: draftthingtypes-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Thing
      - Types
    post:
      summary: Create a draft thing type
      description: |-
        Creates a new draft thing type for the organization in the Watson IoT
        Platform.  The thing type must reference the schema definition that
        defines the structure of instances of the thing type.
      operationId: creates-a-new-draft-thing-type-for-the-organization-in-the-watson-iotplatform--the-thing-type-must-r
      x-api-path-slug: draftthingtypes-post
      parameters:
      - in: body
        name: Thing Type
        description: The JSON representation of the thing type
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Thing
      - Types
  /draft/thing/types/{thingTypeId}:
    get:
      summary: Get a draft thing type
      description: Retrieve the draft thing type with the specified id.
      operationId: retrieve-the-draft-thing-type-with-the-specified-id
      x-api-path-slug: draftthingtypesthingtypeid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Thing
      - Types
      - ThingTypeId
    put:
      summary: Update a draft thing type
      description: "Updates the draft thing type with the specified id. The following\nproperties
        can be updated:\n\n  - name\n  - description\n  - schemaId\n  - metadata\n\nNote
        that if the description field is omitted from the body of the\nupdate, then
        any existing description will be removed from the draft\nthing type.\n  \nAny
        changes made to the values of the following properties will be\nignored:\n\n
        \ - version\n  - created\n  - createdBy\n  - updated\n  - updatedBy\n  - refs\n
        \ \nThe values of these properties are set on the server as a result of a\nsuccessful
        update."
      operationId: updates-the-draft-thing-type-with-the-specified-id-the-followingproperties-can-be-updated---name---d
      x-api-path-slug: draftthingtypesthingtypeid-put
      parameters:
      - in: query
        name: No Name
      - in: body
        name: Thing Type
        description: The JSON representation of the thing type
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Thing
      - Types
      - ThingTypeId
    patch:
      summary: Perform an operation against a draft thing type
      description: "Performs the specified operation against the draft thing type.
        The\nfollowing values can be specified for the operation property:\n\n  -
        validate-configuration\n  - activate-configuration\n  - list-differences\n\nThe
        **validate-configuration** operation will analyze all of the \nconfiguration
        associated with the draft thing type to determine if it is\nvalid.  If the
        configuration is invalid, a list of the issues will be\nreturned in the body
        of the response.  \n \nThe **activate-configuration** operation will make
        the configuration\nassociated with the draft thing type active. The \n**activate-configuration**
        operation must have been performed against a\ndraft thing type before any
        instances of that type can be created.\n\nThe **list-differences** operation
        will return a list of the differences\nthat exist between the active configuration
        for the thing type, if any,\nand the draft configuration."
      operationId: performs-the-specified-operation-against-the-draft-thing-type-thefollowing-values-can-be-specified-f
      x-api-path-slug: draftthingtypesthingtypeid-patch
      parameters:
      - in: query
        name: No Name
      - in: body
        name: Thing Type Operation
        description: The JSON representation of a thing type operation
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Thing
      - Types
      - ThingTypeId
    delete:
      summary: Delete a draft thing type
      description: |-
        Deletes the draft thing type with the specified id from the organization
        in the Watson IoT Platform.

        Please note the the delete will fail if there is an active version of the
        thing type or if the thing type is currently being referenced by another
        object.
      operationId: deletes-the-draft-thing-type-with-the-specified-id-from-the-organizationin-the-watson-iot-platformpl
      x-api-path-slug: draftthingtypesthingtypeid-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Thing
      - Types
      - ThingTypeId
  /thing/types/{thingTypeId}/logicalinterfaces:
    get:
      summary: |-
        Get the list of active logical interfaces associated with the thing
        type
      description: |-
        Retrieve the list of active logical  interfaces that have been associated
        with the thing type.  At least one logical interface must be associated
        with the thing type before any mappings can be defined that will generate
        state for the thing.
      operationId: retrieve-the-list-of-active-logical--interfaces-that-have-been-associatedwith-the-thing-type--at-lea
      x-api-path-slug: thingtypesthingtypeidlogicalinterfaces-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Thing
      - Types
      - ThingTypeId
      - Logical interfaces
  /thing/types/{thingTypeId}/mappings:
    get:
      summary: Get the list of active property mappings for the thing type
      description: |-
        Retrieve the list of active property mappings for the specified thing
        type.  A property mapping defines how properties from state update events
        on aggregated devices or things are mapped to properties defined on a
        logical interface associated with the thing type.
      operationId: retrieve-the-list-of-active-property-mappings-for-the-specified-thingtype--a-property-mapping-define
      x-api-path-slug: thingtypesthingtypeidmappings-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Thing
      - Types
      - ThingTypeId
      - Mappings
  /thing/types/{thingTypeId}/mappings/{logicalInterfaceId}:
    get:
      summary: |-
        Get the active property mappings for a specific logical interface for
        a thing type.
      description: |-
        Retrieves the active property mappings for a specific logical interface
        for the thing type.
      operationId: retrieves-the-active-property-mappings-for-a-specific-logical-interfacefor-the-thing-type
      x-api-path-slug: thingtypesthingtypeidmappingslogicalinterfaceid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Thing
      - Types
      - ThingTypeId
      - Mappings
      - LogicalInterfaceId
  /draft/thing/types/{thingTypeId}/logicalinterfaces:
    get:
      summary: |-
        Get the list of draft logical interfaces associated with the thing
        type
      description: |-
        Retrieve the list of draft logical interfaces that have been associated
        with the draft thing type.  At least one logical interface must be
        associated with the thing type before any mappings can be defined that
        will generate state for the thing.
      operationId: retrieve-the-list-of-draft-logical-interfaces-that-have-been-associatedwith-the-draft-thing-type--at
      x-api-path-slug: draftthingtypesthingtypeidlogicalinterfaces-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Thing
      - Types
      - ThingTypeId
      - Logical interfaces
    post:
      summary: Associate a draft logical interface with the draft thing type
      description: |-
        Associates a draft logical interface with the specified draft thing type.
        The logical interface must already exist within the organization in the
        Watson IoT Platform.
      operationId: associates-a-draft-logical-interface-with-the-specified-draft-thing-typethe-logical-interface-must-a
      x-api-path-slug: draftthingtypesthingtypeidlogicalinterfaces-post
      parameters:
      - in: body
        name: Logical Interface
        description: The JSON representation of the draft logical interface
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Thing
      - Types
      - ThingTypeId
      - Logical interfaces
  /draft/thing/types/{thingTypeId}/logicalinterfaces/{logicalInterfaceId}:
    delete:
      summary: Disassociate a logical interface from the draft thing type
      description: |-
        Disassociates the draft logical interface with the specified id from the
        draft thing type.

        Please note the the delete will fail if the logical interface being
        removed from the draft thing type is referenced in the property mappings
        for the draft thing type.
      operationId: disassociates-the-draft-logical-interface-with-the-specified-id-from-thedraft-thing-typeplease-note-
      x-api-path-slug: draftthingtypesthingtypeidlogicalinterfaceslogicalinterfaceid-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Thing
      - Types
      - ThingTypeId
      - Logical interfaces
      - LogicalInterfaceId
  /draft/thing/types/{thingTypeId}/mappings:
    get:
      summary: Get the list of draft property mappings for the thing type
      description: |-
        Retrieve the list of draft property mappings for the specified draft
        thing type.  A property mapping defines how properties from state update
        events on aggregated devices or things are mapped to properties defined
        on a logical interface associated with the thing type.
      operationId: retrieve-the-list-of-draft-property-mappings-for-the-specified-draftthing-type--a-property-mapping-d
      x-api-path-slug: draftthingtypesthingtypeidmappings-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Thing
      - Types
      - ThingTypeId
      - Mappings
    post:
      summary: |-
        Create the draft property mappings for a logical interface for the thing
        type
      description: |-
        Creates the draft property mappings for a logical interface for the
        thing type.  The mapping object must specify:
        - The id for for the logical interface that the mappings are for
        - The mappings that define how to map from properties on the state
          update events to the properties on the logical interface.  The
          mappings are keyed off of the name of the internal properties of the
          thing type.
      operationId: creates-the-draft-property-mappings-for-a-logical-interface-for-thething-type--the-mapping-object-mu
      x-api-path-slug: draftthingtypesthingtypeidmappings-post
      parameters:
      - in: query
        name: No Name
      - in: body
        name: Thing Type Property Mappings
        description: The JSON representation of the thing type property mappings
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Thing
      - Types
      - ThingTypeId
      - Mappings
  /draft/thing/types/{thingTypeId}/mappings/{logicalInterfaceId}:
    get:
      summary: |-
        Get the draft property mappings for a specific logical interface for
        a thing type.
      description: |-
        Retrieves the draft property mappings for a specific logical interface
        for the thing type.
      operationId: retrieves-the-draft-property-mappings-for-a-specific-logical-interfacefor-the-thing-type
      x-api-path-slug: draftthingtypesthingtypeidmappingslogicalinterfaceid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Thing
      - Types
      - ThingTypeId
      - Mappings
      - LogicalInterfaceId
    put:
      summary: |-
        Update the property mappings for a specific logical interface for
        the thing type.
      description: |-
        Updates the property mappings for a specific logical interface
        for the draft thing type.
      operationId: updates-the-property-mappings-for-a-specific-logical-interfacefor-the-draft-thing-type
      x-api-path-slug: draftthingtypesthingtypeidmappingslogicalinterfaceid-put
      parameters:
      - in: query
        name: No Name
      - in: body
        name: Thing Type Property Mappings
        description: The JSON representation of the thing type property mappings
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Thing
      - Types
      - ThingTypeId
      - Mappings
      - LogicalInterfaceId
    delete:
      summary: |-
        Delete the property mappings for a specific logical interface for
        the draft thing type.
      description: |-
        Deletes the property mappings for a specific logical interface
        for the draft thing type.
      operationId: deletes-the-property-mappings-for-a-specific-logical-interfacefor-the-draft-thing-type
      x-api-path-slug: draftthingtypesthingtypeidmappingslogicalinterfaceid-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Thing
      - Types
      - ThingTypeId
      - Mappings
      - LogicalInterfaceId
  /thing/types/{thingTypeId}/things:
    get:
      summary: List things
      description: "Within the Watson IoT Platform, a Thing allows you to aggregate
        one or\nmore instances of a Device or Thing together to represent a more coarse\ngrained
        object.  For example, you might aggregrate together a\ntemperature sensor,
        flow sensor and power sensor together into a Boiler. \n\nThe **/thing/types/{thingTypeId}/things**
        endpoint returns the list of\nall of the Thing instances of the specified
        type that have been created\nfor the organization in the Watson IoT Platform.
        Various query\nparameters can be used to filter, sort and page through the
        list of\nThing instances that are returned."
      operationId: within-the-watson-iot-platform-a-thing-allows-you-to-aggregate-one-ormore-instances-of-a-device-or-t
      x-api-path-slug: thingtypesthingtypeidthings-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Thing
      - Types
      - ThingTypeId
      - Things
    post:
      summary: Create a thing
      description: "Creates a thing instance of the specified type for the organization
        in\nthe Watson IoT Platform. The thing type must have a valid set of   \nInformation
        Management metadata associated with it and activated before\nany instances
        can be created."
      operationId: creates-a-thing-instance-of-the-specified-type-for-the-organization-inthe-watson-iot-platform-the-th
      x-api-path-slug: thingtypesthingtypeidthings-post
      parameters:
      - in: query
        name: No Name
      - in: body
        name: thing
        description: Thing to be created
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Thing
      - Types
      - ThingTypeId
      - Things
  /thing/types/{thingTypeId}/things/{thingId}:
    get:
      summary: Get a thing
      description: Retrieve the thing with the specified id.
      operationId: retrieve-the-thing-with-the-specified-id
      x-api-path-slug: thingtypesthingtypeidthingsthingid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Thing
      - Types
      - ThingTypeId
      - Things
      - ThingId
    put:
      summary: Update a thing
      description: "Updates the thing with the specified id. The following properties\ncan
        be updated:\n\n  - name\n  - description\n  - metadata\n  - aggregatedObjects\n\nNote
        that if the description field is omitted from the body of the\nupdate, then
        any existing description will be removed from the thing\ntype.\n  \nAny changes
        made to the values of the following properties will be\nignored:\n\n  - created\n
        \ - createdBy\n  - updated\n  - updatedBy\n  \nThe values of these properties
        are set on the server as a result of a\nsuccessful update."
      operationId: updates-the-thing-with-the-specified-id-the-following-propertiescan-be-updated---name---description-
      x-api-path-slug: thingtypesthingtypeidthingsthingid-put
      parameters:
      - in: query
        name: No Name
      - in: body
        name: Thing
        description: The JSON representation of the thing
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Thing
      - Types
      - ThingTypeId
      - Things
      - ThingId
    delete:
      summary: Delete a thing
      description: "Deletes the thing with the specified id from the organization
        in the \nWatson IoT Platform.\n\nPlease note the the delete will fail if the
        thing being deleted is \ncurrently being aggregated by other thing instances."
      operationId: deletes-the-thing-with-the-specified-id-from-the-organization-in-the-watson-iot-platformplease-note-
      x-api-path-slug: thingtypesthingtypeidthingsthingid-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Thing
      - Types
      - ThingTypeId
      - Things
      - ThingId
  /thing/types/{thingTypeId}/things/{thingId}/state/{logicalInterfaceId}:
    get:
      summary: Get the state for the thing with the specified id
      description: Retrieve the current state of the thing with the specified id.
      operationId: retrieve-the-current-state-of-the-thing-with-the-specified-id
      x-api-path-slug: thingtypesthingtypeidthingsthingidstatelogicalinterfaceid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Thing
      - Types
      - ThingTypeId
      - Things
      - ThingId
      - State
      - LogicalInterfaceId
    patch:
      summary: Perform an operation against the thing state for a logical interface
      description: |-
        Performs the specified operation against the thing state for a logical
        interface. The following values can be specified for the operation
        property:

          - reset-state

        The **reset-state** operation will reset the state of the specified
        thing instance to the default values as defined by the schema for the
        logical interface.
      operationId: performs-the-specified-operation-against-the-thing-state-for-a-logicalinterface-the-following-values
      x-api-path-slug: thingtypesthingtypeidthingsthingidstatelogicalinterfaceid-patch
      parameters:
      - in: query
        name: No Name
      - in: body
        name: Operation
        description: The JSON representation of an operation
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Thing
      - Types
      - ThingTypeId
      - Things
      - ThingId
      - State
      - LogicalInterfaceId
  /identity/token:
    get:
      summary: Get Entity Token
      description: Tokens are required for the ML REST API authentication. They are
        generated using ML service credentials
      operationId: generateToken
      x-api-path-slug: identitytoken-get
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Identity
      - Token
    put:
      summary: Put Entity Token
      description: Refreshes token, accepts expired token and generates a new one
        (if the application binding / service key is still valid)
      operationId: refreshes-token-accepts-expired-token-and-generates-a-new-one-if-the-application-binding--service-ke
      x-api-path-slug: identitytoken-put
      parameters:
      - in: body
        name: token
        description: existing token
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Identity
      - Token
  /wml_instances/{instance_id}/published_models:
    get:
      summary: Get Wml Instances Instance Published Models
      description: Get wml instances instance published models.
      operationId: listModelDeployments
      x-api-path-slug: wml-instancesinstance-idpublished-models-get
      parameters:
      - in: query
        name: limit
        description: Maximum number of resources to retrive (defaults to 1000)
      - in: query
        name: start
        description: Token required for token-based pagination
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
  /wml_instances/{instance_id}/published_models/{published_model_id}:
    get:
      summary: Get Wml Instances Instance Published Models Published Model
      description: Get wml instances instance published models published model.
      operationId: details-about-specific-published-model
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-id-get
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
    delete:
      summary: Delete Wml Instances Instance Published Models Published Model
      description: Delete wml instances instance published models published model.
      operationId: deletes-the-published-model-and-all-its-deployments
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-id-delete
      parameters:
      - in: query
        name: ignore_spark_errors
        description: If this flag is set to true then deployments of this model will
          be deleted even if spark reports failure in response to kill job request
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
    patch:
      summary: Patch Wml Instances Instance Published Models Published Model
      description: Patch wml instances instance published models published model.
      operationId: updates-the-version-of-deployed-model
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-id-patch
      parameters:
      - in: body
        name: published_model_patch
        description: Input For Patch
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
  /wml_instances/{instance_id}/published_models/{published_model_id}/evaluation_metrics:
    get:
      summary: Get Wml Instances Instance Published Models Published Model Evaluation
        Metrics
      description: Get wml instances instance published models published model evaluation
        metrics.
      operationId: listModelMetrics
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-idevaluation-metrics-get
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Evaluation
      - Metrics
  /wml_instances/{instance_id}/published_models/{published_model_id}/learning_configuration:
    put:
      summary: Put Wml Instances Instance Published Models Published Model Learning
        Configuration
      description: Put wml instances instance published models published model learning
        configuration.
      operationId: creates-learning-configuration
      x-api-path-slug: wml-instancesinstance-idpublished-modelspublished-model-idlearning-configuration-put
      parameters:
      - in: body
        name: learning_configuration
        description: The model deployment Id
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Machine Learning
      - Wml
      - Instances
      - Instance
      - Id
      - Published
      - Models
      - Published
      - Model
      - Id
      - Learning
      - Configuration
host: ibm-watson-ml.mybluemix.net
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---