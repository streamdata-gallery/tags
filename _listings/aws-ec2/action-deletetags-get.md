---
swagger: "2.0"
info:
  title: AWS EC2 API Delete Tags
  version: 1.0.0
  description: Deletes the specified set of tags from the specified set of resources.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DeleteTags:
    get:
      summary: Delete Tags
      description: Deletes the specified set of tags from the specified set of resources
      operationId: deletetags
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
        name: MaxResults
        description: The maximum number of results to return in a single call
        type: string
      - in: query
        name: NextToken
        description: The token to retrieve the next page of results
        type: string
      responses:
        200:
          description: OK
      tags:
      - tags
definitions: []
x-collection-name: AWS EC2
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