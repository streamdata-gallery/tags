---
swagger: "2.0"
x-collection-name: TidyHQ
x-complete: 0
info:
  title: API Evangelist Building Block API Get Tags for Building Block
  description: building block tags
  contact:
    name: Kin Lane
    url: http://kinlane.com
    email: info@kinlane.com
  version: v1
host: buildingblock.api.kinlane.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /buildingblocks/{building_block_id}/tags/:
    get:
      summary: Get Tags for Building Block
      description: building block tags
      operationId: getbuildingblockTags
      x-api-path-slug: buildingblocksbuilding-block-idtags-get
      parameters:
      - in: query
        name: appid
        description: your appid for accessing the building block
      - in: query
        name: appkey
        description: your appkey for accessing the building block
      - in: path
        name: building_block_id
        description: id for building block
      responses:
        200:
          description: OK
      tags:
      - TagsBuilding
      - Block
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