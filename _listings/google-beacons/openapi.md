---
swagger: "2.0"
x-collection-name: Google Beacons
x-complete: 1
info:
  title: Google Proximity Beacon
  description: registers-manages-indexes-and-searches-beacons-
  contact:
    name: Google
    url: https://google.com
  version: v1beta1
host: proximitybeacon.googleapis.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1beta1/namespaces:
    get:
      summary: Get Namespace
      description: |-
        Lists all attachment namespaces owned by your Google Developers Console
        project. Attachment data associated with a beacon must include a
        namespaced type, and the namespace must be owned by your project.

        Authenticate using an [OAuth access token](https://developers.google.com/identity/protocols/OAuth2)
        from a signed-in user with **viewer**, **Is owner** or **Can edit**
        permissions in the Google Developers Console project.
      operationId: proximitybeacon.namespaces.list
      x-api-path-slug: v1beta1namespaces-get
      parameters:
      - in: query
        name: projectId
        description: The project id to list namespaces under
      responses:
        200:
          description: OK
      tags:
      - Namespace
  /v1beta1/{attachmentName}:
    delete:
      summary: Delete Attachment
      description: |-
        Deletes the specified attachment for the given beacon. Each attachment has
        a unique attachment name (`attachmentName`) which is returned when you
        fetch the attachment data via this API. You specify this with the delete
        request to control which attachment is removed. This operation cannot be
        undone.

        Authenticate using an [OAuth access token](https://developers.google.com/identity/protocols/OAuth2)
        from a signed-in user with **Is owner** or **Can edit** permissions in the
        Google Developers Console project.
      operationId: proximitybeacon.beacons.attachments.delete
      x-api-path-slug: v1beta1attachmentname-delete
      parameters:
      - in: path
        name: attachmentName
        description: The attachment name (`attachmentName`) ofthe attachment to remove
      - in: query
        name: projectId
        description: The project id of the attachment to delete
      responses:
        200:
          description: OK
      tags:
      - Attachment
  /v1beta1/{beaconName}/attachments:
    get:
      summary: Get Attachments
      description: |-
        Returns the attachments for the specified beacon that match the specified
        namespaced-type pattern.

        To control which namespaced types are returned, you add the
        `namespacedType` query parameter to the request. You must either use
        `*/*`, to return all attachments, or the namespace must be one of
        the ones returned from the  `namespaces` endpoint.

        Authenticate using an [OAuth access token](https://developers.google.com/identity/protocols/OAuth2)
        from a signed-in user with **viewer**, **Is owner** or **Can edit**
        permissions in the Google Developers Console project.
      operationId: proximitybeacon.beacons.attachments.list
      x-api-path-slug: v1beta1beaconnameattachments-get
      parameters:
      - in: path
        name: beaconName
        description: Beacon whose attachments should be fetched
      - in: query
        name: namespacedType
        description: Specifies the namespace and type of attachment to include in
          response innamespace/type format
      - in: query
        name: projectId
        description: The project id to list beacon attachments under
      responses:
        200:
          description: OK
      tags:
      - Attachment
    post:
      summary: Add Attachment
      description: |-
        Associates the given data with the specified beacon. Attachment data must
        contain two parts:
        <ul>
        <li>A namespaced type.</li>
        <li>The actual attachment data itself.</li>
        </ul>
        The namespaced type consists of two parts, the namespace and the type.
        The namespace must be one of the values returned by the `namespaces`
        endpoint, while the type can be a string of any characters except for the
        forward slash (`/`) up to 100 characters in length.

        Attachment data can be up to 1024 bytes long.

        Authenticate using an [OAuth access token](https://developers.google.com/identity/protocols/OAuth2)
        from a signed-in user with **Is owner** or **Can edit** permissions in the
        Google Developers Console project.
      operationId: proximitybeacon.beacons.attachments.create
      x-api-path-slug: v1beta1beaconnameattachments-post
      parameters:
      - in: path
        name: beaconName
        description: Beacon on which the attachment should be created
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: projectId
        description: The project id of the project the attachment will belong to
      responses:
        200:
          description: OK
      tags:
      - Attachment
  /v1beta1/{beaconName}/attachments:batchDelete:
    post:
      summary: Delete Attachments
      description: |-
        Deletes multiple attachments on a given beacon. This operation is
        permanent and cannot be undone.

        You can optionally specify `namespacedType` to choose which attachments
        should be deleted. If you do not specify `namespacedType`,  all your
        attachments on the given beacon will be deleted. You also may explicitly
        specify `*/*` to delete all.

        Authenticate using an [OAuth access token](https://developers.google.com/identity/protocols/OAuth2)
        from a signed-in user with **Is owner** or **Can edit** permissions in the
        Google Developers Console project.
      operationId: proximitybeacon.beacons.attachments.batchDelete
      x-api-path-slug: v1beta1beaconnameattachmentsbatchdelete-post
      parameters:
      - in: path
        name: beaconName
        description: The beacon whose attachments should be deleted
      - in: query
        name: namespacedType
        description: Specifies the namespace and type of attachments to delete in`namespace/type`
          format
      - in: query
        name: projectId
        description: The project id to delete beacon attachments under
      responses:
        200:
          description: OK
      tags:
      - Attachment
  /v1beta1/{namespaceName}:
    put:
      summary: Update Namespace
      description: |-
        Updates the information about the specified namespace. Only the namespace
        visibility can be updated.
      operationId: proximitybeacon.namespaces.update
      x-api-path-slug: v1beta1namespacename-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: namespaceName
        description: Resource name of this namespace
      - in: query
        name: projectId
        description: The project id of the namespace to update
      responses:
        200:
          description: OK
      tags:
      - Namespace
---