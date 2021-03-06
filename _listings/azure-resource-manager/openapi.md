swagger: "2.0"
x-collection-name: Azure Resource Manager
x-complete: 1
info:
  title: SubscriptionClient
  description: all-resource-groups-and-resources-exist-within-subscriptions--these-operation-enable-you-get-information-about-your-subscriptions-and-tenants--a-tenant-is-a-dedicated-instance-of-azure-active-directory-azure-ad-for-your-organization-
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
  /subscriptions/{subscriptionId}/tagNames/{tagName}/tagValues/{tagValue}:
    delete:
      summary: Tags Delete Value
      description: Deletes a tag value.
      operationId: Tags_DeleteValue
      x-api-path-slug: subscriptionssubscriptionidtagnamestagnametagvaluestagvalue-delete
      parameters:
      - in: query
        name: No Name
      - in: path
        name: tagName
        description: The name of the tag
      - in: path
        name: tagValue
        description: The value of the tag to delete
      responses:
        200:
          description: OK
      tags:
      - Tags
    put:
      summary: Tags Create Or Update Value
      description: Creates a tag value. The name of the tag must already exist.
      operationId: Tags_CreateOrUpdateValue
      x-api-path-slug: subscriptionssubscriptionidtagnamestagnametagvaluestagvalue-put
      parameters:
      - in: query
        name: No Name
      - in: path
        name: tagName
        description: The name of the tag
      - in: path
        name: tagValue
        description: The value of the tag to create
      responses:
        200:
          description: OK
      tags:
      - Tags
  /subscriptions/{subscriptionId}/tagNames/{tagName}:
    put:
      summary: Creates a tag in the subscription.
      description: The tag name can have a maximum of 512 characters and is case insensitive.
        Tag names created by Azure have prefixes of microsoft, azure, or windows.
        You cannot create tags with one of these prefixes.
      operationId: Tags_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidtagnamestagname-put
      parameters:
      - in: query
        name: No Name
      - in: path
        name: tagName
        description: The name of the tag to create
      responses:
        200:
          description: OK
      tags:
      - Tags
    delete:
      summary: Deletes a tag from the subscription.
      description: You must remove all values from a resource tag before you can delete
        it.
      operationId: Tags_Delete
      x-api-path-slug: subscriptionssubscriptionidtagnamestagname-delete
      parameters:
      - in: query
        name: No Name
      - in: path
        name: tagName
        description: The name of the tag
      responses:
        200:
          description: OK
      tags:
      - Tags
  /subscriptions/{subscriptionId}/tagNames:
    get:
      summary: Tags List
      description: Gets the names and values of all resource tags that are defined
        in a subscription.
      operationId: Tags_List
      x-api-path-slug: subscriptionssubscriptionidtagnames-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Tags