---
swagger: "2.0"
x-collection-name: Etsy
x-complete: 0
info:
  title: Etsy Get Taxonomy Tags Tags
  description: Retrieves all related tags for the given tag set.
  version: 1.0.0
host: openapi.etsy.com
basePath: /v2/private/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /taxonomy/tags:
    get:
      summary: Get Taxonomy Tags
      description: Retrieves all related tags for the given tag set.
      operationId: getTaxonomyTags
      x-api-path-slug: taxonomytags-get
      parameters:
      - in: query
        name: limit
        description: Bring Etsys handmade marketplace and community into your apps
      responses:
        200:
          description: OK
      tags:
      - Taxonomy
      - Tags
  /taxonomy/tags/{tags}:
    get:
      summary: Get Taxonomy Tags Tags
      description: Retrieves all related tags for the given tag set.
      operationId: getTaxonomyTagsTags
      x-api-path-slug: taxonomytagstags-get
      parameters:
      - in: query
        name: limit
        description: Bring Etsys handmade marketplace and community into your apps
      - in: path
        name: tags
      responses:
        200:
          description: OK
      tags:
      - Taxonomy
      - Tags
      - Tags
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