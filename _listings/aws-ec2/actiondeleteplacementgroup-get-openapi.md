---
swagger: "2.0"
x-collection-name: AWS EC2
x-complete: 0
info:
  title: AWS EC2 API Delete Placement Group
  version: 1.0.0
  description: Deletes the specified placement group.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DeleteCustomerGateway:
    get:
      summary: Delete Customer Gateway
      description: Deletes the specified customer gateway.
      operationId: deletecustomergateway
      x-api-path-slug: actiondeletecustomergateway-get
      parameters:
      - in: query
        name: CustomerGatewayId.N
        description: One or more customer gateway IDs
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,             and provides an error response
        type: string
      - in: query
        name: Filter.N
        description: One or more filters
        type: string
      responses:
        200:
          description: OK
      tags:
      - Customer Gateway
  /?Action=DescribeCustomerGateways:
    get:
      summary: Describe Customer Gateways
      description: Describes one or more of your VPN customer gateways.
      operationId: describecustomergateways
      x-api-path-slug: actiondescribecustomergateways-get
      parameters:
      - in: query
        name: AutoPlacement
        description: This is enabled by default
        type: string
      - in: query
        name: AvailabilityZone
        description: The Availability Zone for the Dedicated Hosts
        type: string
      - in: query
        name: ClientToken
        description: Unique, case-sensitive identifier you provide to ensure idempotency
          of the request
        type: string
      - in: query
        name: InstanceType
        description: Specify the instance type that you want your Dedicated Hosts
          to be configured for
        type: string
      - in: query
        name: Quantity
        description: The number of Dedicated Hosts you want to allocate to your account
          with these            parameters
        type: string
      responses:
        200:
          description: OK
      tags:
      - Customer Gateways
  /?Action=AttachVolume:
    get:
      summary: Attach Volume
      description: |-
        Attaches an EBS volume to a running or stopped instance and exposes it to the instance with
              the specified device name.
      operationId: attachvolume
      x-api-path-slug: actionattachvolume-get
      parameters:
      - in: query
        name: Description
        description: A description for the EBS snapshot
        type: string
      - in: query
        name: DestinationRegion
        description: The destination region to use in the PresignedUrl parameter of
          a snapshot copy      operation
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the      request, and provides an error response
        type: string
      - in: query
        name: Encrypted
        description: Specifies whether the destination snapshot should be encrypted
        type: string
      - in: query
        name: KmsKeyId
        description: The full ARN of the AWS Key Management Service (AWS KMS) CMK
          to use when creating the snapshot copy
        type: string
      - in: query
        name: PresignedUrl
        description: The pre-signed URL that facilitates copying an encrypted snapshot
        type: string
      - in: query
        name: SourceRegion
        description: The ID of the region that contains the snapshot to be copied
        type: string
      - in: query
        name: SourceSnapshotId
        description: The ID of the EBS snapshot to copy
        type: string
      responses:
        200:
          description: OK
      tags:
      - Drive Volume
  /?Action=CreateVolume:
    get:
      summary: Create Volume
      description: Creates an EBS volume that can be attached to an instance in the
        same Availability Zone.
      operationId: createvolume
      x-api-path-slug: actioncreatevolume-get
      parameters:
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the      request, and provides an error response
        type: string
      - in: query
        name: SnapshotId
        description: The ID of the EBS snapshot
        type: string
      responses:
        200:
          description: OK
      tags:
      - Volume
  /?Action=DeleteVolume:
    get:
      summary: Delete Volume
      description: Deletes the specified EBS volume.
      operationId: deletevolume
      x-api-path-slug: actiondeletevolume-get
      parameters:
      - in: query
        name: Attribute
        description: The snapshot attribute you would like to view
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the      request, and provides an error response
        type: string
      - in: query
        name: SnapshotId
        description: The ID of the EBS snapshot
        type: string
      responses:
        200:
          description: OK
      tags:
      - Volume
  /?Action=DescribeVolumeAttribute:
    get:
      summary: Describe Volume Attribute
      description: Describes the specified attribute of the specified volume.
      operationId: describevolumeattribute
      x-api-path-slug: actiondescribevolumeattribute-get
      parameters:
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the      request, and provides an error response
        type: string
      - in: query
        name: Filter.N
        description: One or more filters
        type: string
      - in: query
        name: MaxResults
        description: The maximum number of volume results returned by DescribeVolumes
          in paginated      output
        type: string
      - in: query
        name: NextToken
        description: The NextToken value returned from a previous paginated        DescribeVolumes
          request where MaxResults was used and the results      exceeded the value
          of that parameter
        type: string
      - in: query
        name: VolumeId.N
        description: One or more volume IDs
        type: string
      responses:
        200:
          description: OK
      tags:
      - Volumes
  /?Action=DescribeVolumes:
    get:
      summary: Describe Volumes
      description: Describes the specified EBS volumes.
      operationId: describevolumes
      x-api-path-slug: actiondescribevolumes-get
      parameters:
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the      request, and provides an error response
        type: string
      - in: query
        name: Filter.N
        description: One or more filters
        type: string
      - in: query
        name: MaxResults
        description: The maximum number of volume results returned by DescribeVolumeStatus
          in      paginated output
        type: string
      - in: query
        name: NextToken
        description: The NextToken value to include in a future DescribeVolumeStatus      request
        type: string
      - in: query
        name: VolumeId.N
        description: One or more volume IDs
        type: string
      responses:
        200:
          description: OK
      tags:
      - Volumes
  /?Action=DescribeVolumeStatus:
    get:
      summary: Describe Volume Status
      description: Describes the status of the specified volumes.
      operationId: describevolumestatus
      x-api-path-slug: actiondescribevolumestatus-get
      parameters:
      - in: query
        name: Device
        description: The device name
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the      request, and provides an error response
        type: string
      - in: query
        name: Force
        description: Forces detachment if the previous detachment attempt did not
          occur cleanly (for example,      logging into an instance, unmounting the
          volume, and detaching normally)
        type: string
      - in: query
        name: InstanceId
        description: The ID of the instance
        type: string
      - in: query
        name: VolumeId
        description: The ID of the volume
        type: string
      responses:
        200:
          description: OK
      tags:
      - Volume Status
  /?Action=DetachVolume:
    get:
      summary: Detach Volume
      description: Detaches an EBS volume from an instance.
      operationId: detachvolume
      x-api-path-slug: actiondetachvolume-get
      parameters:
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the      request, and provides an error response
        type: string
      - in: query
        name: VolumeId
        description: The ID of the volume
        type: string
      responses:
        200:
          description: OK
      tags:
      - Volume
  /?Action=EnableVolumeIO:
    get:
      summary: Enable Volume I O
      description: |-
        Enables I/O operations for a volume that had I/O operations disabled because the data on the
              volume was potentially inconsistent.
      operationId: enablevolumeio
      x-api-path-slug: actionenablevolumeio-get
      parameters:
      - in: query
        name: Attribute
        description: The snapshot attribute to modify
        type: string
      - in: query
        name: CreateVolumePermission
        description: A JSON representation of the snapshot attribute modification
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the      request, and provides an error response
        type: string
      - in: query
        name: OperationType
        description: The type of operation to perform to the attribute
        type: string
      - in: query
        name: SnapshotId
        description: The ID of the snapshot
        type: string
      - in: query
        name: UserGroup.N
        description: The group to modify for the snapshot
        type: string
      - in: query
        name: UserId.N
        description: The account ID to modify for the snapshot
        type: string
      responses:
        200:
          description: OK
      tags:
      - Volumes
  /?Action=ModifyVolumeAttribute:
    get:
      summary: Modify Volume Attribute
      description: Modifies a volume attribute.
      operationId: modifyvolumeattribute
      x-api-path-slug: actionmodifyvolumeattribute-get
      parameters:
      - in: query
        name: Attribute
        description: The attribute to reset
        type: string
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the      request, and provides an error response
        type: string
      - in: query
        name: SnapshotId
        description: The ID of the snapshot
        type: string
      responses:
        200:
          description: OK
      tags:
      - Volume
  /?Action=CreatePlacementGroup:
    get:
      summary: Create Placement Group
      description: Creates a placement group that you launch cluster instances into.
      operationId: createplacementgroup
      x-api-path-slug: actioncreateplacementgroup-get
      parameters:
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,        and provides an error response
        type: string
      - in: query
        name: GroupName
        description: The name of the placement group
        type: string
      responses:
        200:
          description: OK
      tags:
      - Placement Group
  /?Action=DeletePlacementGroup:
    get:
      summary: Delete Placement Group
      description: Deletes the specified placement group.
      operationId: deleteplacementgroup
      x-api-path-slug: actiondeleteplacementgroup-get
      parameters:
      - in: query
        name: DryRun
        description: Checks whether you have the required permissions for the action,
          without actually making the request,        and provides an error response
        type: string
      - in: query
        name: Filter.N
        description: One or more filters
        type: string
      - in: query
        name: GroupName.N
        description: One or more placement group names
        type: string
      responses:
        200:
          description: OK
      tags:
      - Placement Group
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