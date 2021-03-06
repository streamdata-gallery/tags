---
swagger: "2.0"
x-collection-name: Click Meter
x-complete: 0
info:
  title: Click Meter List of all the groups associated to the user filtered by this
    tag.
  description: List of all the groups associated to the user filtered by this tag..
  contact:
    name: Api Support
    url: http://www.clickmeter.com/api
    email: api@clickmeter.com
  version: v2
host: apiv2.clickmeter.com:80
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /tags:
    get:
      summary: List of all the groups associated to the user filtered by this tag.
      description: List of all the groups associated to the user filtered by this
        tag..
      operationId: getTags
      x-api-path-slug: tags-get
      parameters:
      - in: query
        name: datapoints
        description: Comma separated list of datapoints id to filter by
      - in: query
        name: groups
        description: Comma separated list of groups id to filter by
      - in: query
        name: limit
        description: Maximum elements to retrieve
      - in: query
        name: name
        description: Name of the tag
      - in: query
        name: offset
        description: Where to start when retrieving elements
      - in: query
        name: type
        description: Type of entity related to the tag
      responses:
        200:
          description: OK
      tags:
      - Tags
    post:
      summary: Create a tag
      description: Create a tag.
      operationId: postTags
      x-api-path-slug: tags-post
      parameters:
      - in: body
        name: value
        description: The body of the tag
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Tags
  /tags/count:
    get:
      summary: List of all the groups associated to the user filtered by this tag.
      description: List of all the groups associated to the user filtered by this
        tag..
      operationId: getTagsCount
      x-api-path-slug: tagscount-get
      parameters:
      - in: query
        name: datapoints
        description: Comma separated list of datapoints id to filter by
      - in: query
        name: groups
        description: Comma separated list of groups id to filter by
      - in: query
        name: name
        description: Name of the tag
      - in: query
        name: type
        description: Type of entity related to the tag
      responses:
        200:
          description: OK
      tags:
      - Tags
      - Count
  /tags/{tagId}:
    delete:
      summary: Delete a tag
      description: Delete a tag.
      operationId: deleteTagsTag
      x-api-path-slug: tagstagid-delete
      parameters:
      - in: path
        name: tagId
        description: Id of the tag
      responses:
        200:
          description: OK
      tags:
      - Tags
      - TagId
    get:
      summary: Retrieve a tag
      description: Retrieve a tag.
      operationId: getTagsTag
      x-api-path-slug: tagstagid-get
      parameters:
      - in: path
        name: tagId
        description: Id of the tag
      responses:
        200:
          description: OK
      tags:
      - Tags
      - TagId
  /tags/{tagId}/datapoints:
    delete:
      summary: Delete the association of this tag with all datapoints
      description: Delete the association of this tag with all datapoints.
      operationId: deleteTagsTagDatapoints
      x-api-path-slug: tagstagiddatapoints-delete
      parameters:
      - in: path
        name: tagId
        description: Id of the tag
      responses:
        200:
          description: OK
      tags:
      - Tags
      - TagId
      - Datapoints
    get:
      summary: List of all the datapoints associated to the user filtered by this
        tag
      description: List of all the datapoints associated to the user filtered by this
        tag.
      operationId: getTagsTagDatapoints
      x-api-path-slug: tagstagiddatapoints-get
      parameters:
      - in: query
        name: createdAfter
        description: Exclude datapoints created before this date (YYYYMMDD)
      - in: query
        name: createdBefore
        description: Exclude datapoints created after this date (YYYYMMDD)
      - in: query
        name: limit
        description: Maximum elements to retrieve
      - in: query
        name: offset
        description: Where to start when retrieving elements
      - in: query
        name: status
        description: Status of the datapoint
      - in: path
        name: tagId
        description: Id of the tag
      - in: query
        name: textSearch
        description: Filter fields by this pattern
      - in: query
        name: type
        description: Type of the datapoint (tp/tl)
      responses:
        200:
          description: OK
      tags:
      - Tags
      - TagId
      - Datapoints
  /tags/{tagId}/datapoints/count:
    get:
      summary: Count the datapoints associated to the user filtered by this tag
      description: Count the datapoints associated to the user filtered by this tag.
      operationId: getTagsTagDatapointsCount
      x-api-path-slug: tagstagiddatapointscount-get
      parameters:
      - in: query
        name: createdAfter
        description: Exclude datapoints created before this date (YYYYMMDD)
      - in: query
        name: createdBefore
        description: Exclude datapoints created after this date (YYYYMMDD)
      - in: query
        name: status
        description: Status of the datapoint
      - in: path
        name: tagId
        description: Id of the tag
      - in: query
        name: textSearch
        description: Filter fields by this pattern
      - in: query
        name: type
        description: Type of the datapoint (tp/tl)
      responses:
        200:
          description: OK
      tags:
      - Tags
      - TagId
      - Datapoints
      - Count
  /tags/{tagId}/datapoints/patch:
    put:
      summary: Associate/Deassociate a tag with a datapoint
      description: Associate/deassociate a tag with a datapoint.
      operationId: putTagsTagDatapointsPatch
      x-api-path-slug: tagstagiddatapointspatch-put
      parameters:
      - in: body
        name: data
        description: The body patch
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: tagId
        description: Id of the tag
      responses:
        200:
          description: OK
      tags:
      - Tags
      - TagId
      - Datapoints
      - Patch
  /tags/{tagId}/groups:
    delete:
      summary: Delete the association of this tag with all groups
      description: Delete the association of this tag with all groups.
      operationId: deleteTagsTagGroups
      x-api-path-slug: tagstagidgroups-delete
      parameters:
      - in: path
        name: tagId
        description: Id of the tag
      responses:
        200:
          description: OK
      tags:
      - Tags
      - TagId
      - Groups
    get:
      summary: List of all the groups associated to the user filtered by this tag.
      description: List of all the groups associated to the user filtered by this
        tag..
      operationId: getTagsTagGroups
      x-api-path-slug: tagstagidgroups-get
      parameters:
      - in: query
        name: createdAfter
        description: Exclude groups created before this date (YYYYMMDD)
      - in: query
        name: createdBefore
        description: Exclude groups created after this date (YYYYMMDD)
      - in: query
        name: limit
        description: Maximum elements to retrieve
      - in: query
        name: offset
        description: Where to start when retrieving elements
      - in: query
        name: status
        description: Status of the datapoint
      - in: path
        name: tagId
        description: Id of the tag
      - in: query
        name: textSearch
        description: Filter fields by this pattern
      responses:
        200:
          description: OK
      tags:
      - Tags
      - TagId
      - Groups
  /tags/{tagId}/groups/count:
    get:
      summary: Count the groups associated to the user filtered by this tag
      description: Count the groups associated to the user filtered by this tag.
      operationId: getTagsTagGroupsCount
      x-api-path-slug: tagstagidgroupscount-get
      parameters:
      - in: query
        name: createdAfter
        description: Exclude groups created before this date (YYYYMMDD)
      - in: query
        name: createdBefore
        description: Exclude groups created after this date (YYYYMMDD)
      - in: query
        name: status
        description: Status of the datapoint
      - in: path
        name: tagId
        description: Id of the tag
      - in: query
        name: textSearch
        description: Filter fields by this pattern
      responses:
        200:
          description: OK
      tags:
      - Tags
      - TagId
      - Groups
      - Count
  /tags/{tagId}/groups/patch:
    put:
      summary: Associate/Deassociate a tag with a group
      description: Associate/deassociate a tag with a group.
      operationId: putTagsTagGroupsPatch
      x-api-path-slug: tagstagidgroupspatch-put
      parameters:
      - in: body
        name: data
        description: The body patch
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: tagId
        description: Id of the tag
      responses:
        200:
          description: OK
      tags:
      - Tags
      - TagId
      - Groups
      - Patch
  /tags/{tagId}/name:
    put:
      summary: Fast patch a tag name
      description: Fast patch a tag name.
      operationId: putTagsTagName
      x-api-path-slug: tagstagidname-put
      parameters:
      - in: body
        name: data
        description: The body patch
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: tagId
        description: Id of the tag
      responses:
        200:
          description: OK
      tags:
      - Tags
      - TagId
      - Name
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