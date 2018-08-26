---
swagger: "2.0"
x-collection-name: Foursquare
x-complete: 0
info:
  title: Foursquare Post Tips Unmark
  description: /tips/{TIP_ID}/marktodo
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
  /tips/search:
    get:
      summary: Get Tips Search
      description: /tips/add
      operationId: tipsadd
      x-api-path-slug: tipssearch-get
      parameters:
      - in: query
        name: filter
        description: If set to friends, only show nearby tips from friends
      - in: query
        name: limit
        description: Number of results to return, up to 500
      - in: query
        name: ll
        description: Latitude and longitude of the users location
      - in: query
        name: offset
        description: Used to page through results
      - in: query
        name: query
        description: Only find tips matching the given term, cannot be used in conjunction
          with friends filter
      - in: query
        name: v
        description: All requests now accept a v=YYYYMMDD param, which indicates that
          the client is up to date as of the specified date
      responses:
        200:
          description: OK
      tags:
      - Tips
      - Search
  /tips/{TIP_ID}:
    get:
      summary: Get Tips
      description: /checkins/{CHECKIN_ID}/deletecomment
      operationId: checkinscheckin-iddeletecomment
      x-api-path-slug: tipstip-id-get
      parameters:
      - in: query
        name: TIP_ID
        description: ID of tip to retrieve
      - in: path
        name: TIP_ID
      - in: query
        name: v
        description: All requests now accept a v=YYYYMMDD param, which indicates that
          the client is up to date as of the specified date
      responses:
        200:
          description: OK
      tags:
      - Tips
  /tips/{TIP_ID}/done:
    get:
      summary: Get Tips Done
      description: /tips/search
      operationId: tipssearch
      x-api-path-slug: tipstip-iddone-get
      parameters:
      - in: query
        name: limit
        description: Number of results to return, up to 200
      - in: query
        name: offset
        description: Used to page through results
      - in: query
        name: TIP_ID
        description: Identity of a tip to get users who have marked the tip as done
      - in: path
        name: TIP_ID
      - in: query
        name: v
        description: All requests now accept a v=YYYYMMDD param, which indicates that
          the client is up to date as of the specified date
      responses:
        200:
          description: OK
      tags:
      - Tips
      - Done
  /tips/{TIP_ID}/listed:
    get:
      summary: Get Tips Listed
      description: /tips/{TIP_ID}/done
      operationId: tipstip-iddone
      x-api-path-slug: tipstip-idlisted-get
      parameters:
      - in: query
        name: group
        description: Can be created, edited, followed, friends, other
      - in: query
        name: TIP_ID
        description: Identity of a tip to get lists for
      - in: path
        name: TIP_ID
      - in: query
        name: v
        description: All requests now accept a v=YYYYMMDD param, which indicates that
          the client is up to date as of the specified date
      responses:
        200:
          description: OK
      tags:
      - Tips
      - Listed
  /tips/{TIP_ID}/markdone:
    post:
      summary: Post Tips Markdone
      description: /tips/{TIP_ID}/listed
      operationId: tipstip-idlisted
      x-api-path-slug: tipstip-idmarkdone-post
      parameters:
      - in: query
        name: TIP_ID
        description: The tip you want to mark done
      - in: path
        name: TIP_ID
      - in: query
        name: v
        description: All requests now accept a v=YYYYMMDD param, which indicates that
          the client is up to date as of the specified date
      responses:
        200:
          description: OK
      tags:
      - Tips
      - Markdone
  /tips/{TIP_ID}/marktodo:
    post:
      summary: Post Tips Marktodo
      description: /tips/{TIP_ID}/markdone
      operationId: tipstip-idmarkdone
      x-api-path-slug: tipstip-idmarktodo-post
      parameters:
      - in: query
        name: TIP_ID
        description: The tip you want to mark to-do
      - in: path
        name: TIP_ID
      - in: query
        name: v
        description: All requests now accept a v=YYYYMMDD param, which indicates that
          the client is up to date as of the specified date
      responses:
        200:
          description: OK
      tags:
      - Tips
      - Marktodo
  /tips/{TIP_ID}/unmark:
    post:
      summary: Post Tips Unmark
      description: /tips/{TIP_ID}/marktodo
      operationId: tipstip-idmarktodo
      x-api-path-slug: tipstip-idunmark-post
      parameters:
      - in: query
        name: TIP_ID
        description: The tip you want to unmark
      - in: path
        name: TIP_ID
      - in: query
        name: v
        description: All requests now accept a v=YYYYMMDD param, which indicates that
          the client is up to date as of the specified date
      responses:
        200:
          description: OK
      tags:
      - Tips
      - Unmark
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