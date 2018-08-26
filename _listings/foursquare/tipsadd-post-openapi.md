---
swagger: "2.0"
x-collection-name: Foursquare
x-complete: 0
info:
  title: Foursquare Post Tips Add
  description: /tips/{TIP_ID}
  version: 1.0.0
host: api.foursquare.com
basePath: /v2/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /tips/add:
    post:
      summary: Post Tips Add
      description: /tips/{TIP_ID}
      operationId: tipstip-id
      x-api-path-slug: tipsadd-post
      parameters:
      - in: query
        name: broadcast
        description: Whether to broadcast this tip
      - in: query
        name: text
        description: The text of the tip, up to 200 characters
      - in: query
        name: url
        description: A URL related to this tip
      - in: query
        name: v
        description: All requests now accept a v=YYYYMMDD param, which indicates that
          the client is up to date as of the specified date
      - in: query
        name: venueId
        description: The venue where you want to add this tip
      responses:
        200:
          description: OK
      tags:
      - Tips
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