---
swagger: "2.0"
x-collection-name: Azure Event Hubs
x-complete: 0
info:
  title: Azure Event Hubs API Consumer Groups Get
  description: Gets a description for the specified consumer group.
  version: 1.0.0
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /subscriptions/{subscriptionId}/providers/Microsoft.EventHub/CheckNameAvailability:
    post:
      summary: Namespaces Check Name Availability
      description: Check the give Namespace name availability.
      operationId: Namespaces_CheckNameAvailability
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-eventhubchecknameavailability-post
      parameters:
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters to check availability of the given Namespace name
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Namespaces Name Availability
  /subscriptions/{subscriptionId}/providers/Microsoft.EventHub/namespaces:
    get:
      summary: Namespaces List By Subscription
      description: Lists all the available Namespaces within a subscription, irrespective
        of the resource groups.
      operationId: Namespaces_ListBySubscription
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-eventhubnamespaces-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Namespaces Subscription
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.EventHub/namespaces:
    get:
      summary: Namespaces List By Resource Group
      description: Lists the available Namespaces within a resource group.
      operationId: Namespaces_ListByResourceGroup
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespaces-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Namespaces Resource Group
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.EventHub/namespaces/{namespaceName}:
    put:
      summary: Namespaces Create Or Update
      description: Creates or updates a namespace. Once created, this namespace's
        resource manifest is immutable. This operation is idempotent.
      operationId: Namespaces_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacename-put
      parameters:
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters for creating a namespace resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Namespaces
    delete:
      summary: Namespaces Delete
      description: Deletes an existing namespace. This operation also removes all
        associated resources under the namespace.
      operationId: Namespaces_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacename-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Namespaces
    get:
      summary: Namespaces Get
      description: Gets the description of the specified namespace.
      operationId: Namespaces_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacename-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Namespaces
    patch:
      summary: Namespaces Update
      description: Creates or updates a namespace. Once created, this namespace's
        resource manifest is immutable. This operation is idempotent.
      operationId: Namespaces_Update
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacename-patch
      parameters:
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters for updating a namespace resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Namespaces
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.EventHub/namespaces/{namespaceName}/AuthorizationRules
  : get:
      summary: Namespaces List Authorization Rules
      description: Gets a list of authorization rules for a Namespace.
      operationId: Namespaces_ListAuthorizationRules
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacenameauthorizationrules-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Namespaces Authorization Rules
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.EventHub/namespaces/{namespaceName}/AuthorizationRules/{authorizationRuleName}
  : put:
      summary: Namespaces Create Or Update Authorization Rule
      description: Creates or updates an AuthorizationRule for a Namespace.
      operationId: Namespaces_CreateOrUpdateAuthorizationRule
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacenameauthorizationrulesauthorizationrulename-put
      parameters:
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The shared access AuthorizationRule
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Namespaces Authorization Rule
    delete:
      summary: Namespaces Delete Authorization Rule
      description: Deletes an AuthorizationRule for a Namespace.
      operationId: Namespaces_DeleteAuthorizationRule
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacenameauthorizationrulesauthorizationrulename-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Namespaces Authorization Rule
    get:
      summary: Namespaces Get Authorization Rule
      description: Gets an AuthorizationRule for a Namespace by rule name.
      operationId: Namespaces_GetAuthorizationRule
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacenameauthorizationrulesauthorizationrulename-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Namespaces Authorization Rule
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.EventHub/namespaces/{namespaceName}/AuthorizationRules/{authorizationRuleName}/listKeys
  : post:
      summary: Namespaces List Keys
      description: Gets the primary and secondary connection strings for the Namespace.
      operationId: Namespaces_ListKeys
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacenameauthorizationrulesauthorizationrulenamelistkeys-post
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Namespaces Keys
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.EventHub/namespaces/{namespaceName}/AuthorizationRules/{authorizationRuleName}/regenerateKeys
  : post:
      summary: Namespaces Regenerate Keys
      description: Regenerates the primary or secondary connection strings for the
        specified Namespace.
      operationId: Namespaces_RegenerateKeys
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacenameauthorizationrulesauthorizationrulenameregeneratekeys-post
      parameters:
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters required to regenerate the connection string
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Namespaces Regenerate Keys
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.EventHub/namespaces/{namespaceName}/eventhubs/{eventHubName}/consumergroups/{consumerGroupName}
  : put:
      summary: Consumer Groups Create Or Update
      description: Creates or updates an Event Hubs consumer group as a nested resource
        within a Namespace.
      operationId: ConsumerGroups_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacenameeventhubseventhubnameconsumergroupsconsumergroupname-put
      parameters:
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters supplied to create or update a consumer group resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Consumer Groups
    delete:
      summary: Consumer Groups Delete
      description: Deletes a consumer group from the specified Event Hub and resource
        group.
      operationId: ConsumerGroups_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacenameeventhubseventhubnameconsumergroupsconsumergroupname-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Consumer Groups
    get:
      summary: Consumer Groups Get
      description: Gets a description for the specified consumer group.
      operationId: ConsumerGroups_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-eventhubnamespacesnamespacenameeventhubseventhubnameconsumergroupsconsumergroupname-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Consumer Groups
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