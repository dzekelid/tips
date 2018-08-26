---
swagger: "2.0"
x-collection-name: Clover
x-complete: 1
info:
  title: ""
  version: 1.0.0
host: /merchants
basePath: https://api.clover.com
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/merchants/{mId}/tip_suggestions:
    get:
      summary: Get all tip suggestions for a merchant
      description: Get all tip suggestions for a merchant.
      operationId: GetTipSuggestions
      x-api-path-slug: v3merchantsmidtip-suggestions-get
      parameters:
      - in: query
        name: filter
        description: 'Filter fields: [id, name, percentage, enabled]'
      - in: path
        name: mId
        description: Merchant Id
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Tip
      - Suggestions
  /v3/merchants/{mId}/tip_suggestions/{tId}:
    get:
      summary: Get a single tip suggestion
      description: Get a single tip suggestion.
      operationId: GetTipSuggestion
      x-api-path-slug: v3merchantsmidtip-suggestionstid-get
      parameters:
      - in: path
        name: mId
        description: Merchant Id
      - in: path
        name: tId
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Tip
      - Suggestions
      - TId
    post:
      summary: Update a single tip suggestion
      description: Update a single tip suggestion.
      operationId: UpdateTipSuggestion
      x-api-path-slug: v3merchantsmidtip-suggestionstid-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: mId
        description: Merchant Id
      - in: path
        name: tId
      responses:
        200:
          description: OK
      tags:
      - Merchants
      - Tip
      - Suggestions
      - TId
---