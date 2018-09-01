---
swagger: "2.0"
x-collection-name: Request Baskets
x-complete: 0
info:
  title: Request Baskets Get collected requests
  description: Fetches collection of requests collected by this basket.
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
    put:
      summary: Update basket settings
      description: |-
        Updates configuration settings of this basket.

        Special configuration parameters for request forwarding:
          * `insecure_tls` controls certificate verification when forwarding requests. Setting this parameter to `true`
          allows to forward collected HTTP requests via HTTPS protocol even if the forward end-point is configured with
          self-signed TLS/SSL certificate. **Warning:** enabling this feature has known security implications.
          * `expand_path` changes the logic of constructing taget URL when forwarding requests. If this parameter is
          set to `true` the forward URL path will be expanded when original HTTP request contains compound path. For
          example, a basket with name **server1** is configured to forward all requests to `http://server1.intranet:8001/myservice`
          and it has received an HTTP request like `GET http://baskets.example.com/server1/component/123/events?status=OK`
          then depending on `expand_path` settings the request will be forwarded to:
            * `true` => `GET http://server1.intranet:8001/myservice/component/123/events?status=OK`
            * `false` => `GET http://server1.intranet:8001/myservice?status=OK`
      operationId: baskets.name.put
      x-api-path-slug: basketsname-put
      parameters:
      - in: body
        name: config
        description: New configuration to apply
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: name
        description: The basket name
      responses:
        200:
          description: OK
      tags:
      - ""
  /baskets/{name}/requests:
    delete:
      summary: Delete all requests
      description: Deletes all requests collected by this basket.
      operationId: baskets.name.requests.delete
      x-api-path-slug: basketsnamerequests-delete
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
      summary: Get collected requests
      description: Fetches collection of requests collected by this basket.
      operationId: baskets.name.requests.get
      x-api-path-slug: basketsnamerequests-get
      parameters:
      - in: query
        name: in
        description: 'Defines what is taken into account when filtering is applied:
          `body` - search in content body of collected requests,`query` - search among
          query parameters of collected requests, `headers` - search among request
          header values,`any` - search anywhere; default `any`'
      - in: query
        name: max
        description: Maximum number of requests to return; default 20
      - in: path
        name: name
        description: The basket name
      - in: query
        name: q
        description: Query string to filter result, only requests that match the query
          will be included in response
      - in: query
        name: skip
        description: Number of requests to skip; default 0
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