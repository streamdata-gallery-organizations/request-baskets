---
swagger: "2.0"
x-collection-name: Request Baskets
x-complete: 0
info:
  title: Request Baskets Create new basket
  description: Creates a new basket with this name.
  contact:
    name: darklynx
    url: https://github.com/darklynx
  version: "0.5"
host: rbaskets.in
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /baskets:
    get:
      summary: Get baskets
      description: Fetches a list of basket names managed by service. Require master
        token.
      operationId: baskets.get
      x-api-path-slug: baskets-get
      parameters:
      - in: query
        name: max
        description: Maximum number of basket names to return; default 20
      - in: query
        name: q
        description: Query string to filter result, only those basket names that match
          the query will be included in response
      - in: query
        name: skip
        description: Number of basket names to skip; default 0
      responses:
        200:
          description: OK
      tags:
      - ""
  /baskets/{name}:
    delete:
      summary: Delete basket
      description: Permanently deletes this basket and all collected requests.
      operationId: baskets.name.delete
      x-api-path-slug: basketsname-delete
      parameters:
      - in: path
        name: name
        description: The basket name
      responses:
        200:
          description: OK
      tags:
      - ""
    get:
      summary: Get basket settings
      description: Retrieves configuration settings of this basket.
      operationId: baskets.name.get
      x-api-path-slug: basketsname-get
      parameters:
      - in: path
        name: name
        description: The basket name
      responses:
        200:
          description: OK
      tags:
      - ""
    post:
      summary: Create new basket
      description: Creates a new basket with this name.
      operationId: baskets.name.post
      x-api-path-slug: basketsname-post
      parameters:
      - in: body
        name: config
        description: Basket configuration
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: name
        description: The name of new basket
      responses:
        200:
          description: OK
      tags:
      - ""
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