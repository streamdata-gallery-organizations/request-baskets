---
name: Request Baskets
x-slug: request-baskets
description: ""
image: ""
x-kinRank: "7"
x-alexaRank: "0"
tags: Request Baskets
created: "2018-08-31"
modified: "2018-08-31"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/request-baskets/master/_listings/request-baskets/apis.md
specificationVersion: "0.14"
apis:
- name: Request Baskets - Get baskets
  x-api-slug: baskets-get
  description: Fetches a list of basket names managed by service. Require master token.
  image: ""
  humanURL: http://rbaskets.in
  baseURL: https://rbaskets.in//
  tags: Storage, Cache, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/request-baskets/master/_listings/request-baskets/baskets-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/request-baskets/master/_listings/request-baskets/baskets-get-openapi.md
- name: Request Baskets - Delete basket
  x-api-slug: basketsname-delete
  description: Permanently deletes this basket and all collected requests.
  image: ""
  humanURL: http://rbaskets.in
  baseURL: https://rbaskets.in//
  tags: Storage, Cache, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/request-baskets/master/_listings/request-baskets/basketsname-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/request-baskets/master/_listings/request-baskets/basketsname-delete-openapi.md
- name: Request Baskets - Get basket settings
  x-api-slug: basketsname-get
  description: Retrieves configuration settings of this basket.
  image: ""
  humanURL: http://rbaskets.in
  baseURL: https://rbaskets.in//
  tags: Storage, Cache, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/request-baskets/master/_listings/request-baskets/basketsname-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/request-baskets/master/_listings/request-baskets/basketsname-get-openapi.md
- name: Request Baskets - Create new basket
  x-api-slug: basketsname-post
  description: Creates a new basket with this name.
  image: ""
  humanURL: http://rbaskets.in
  baseURL: https://rbaskets.in//
  tags: Storage, Cache, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/request-baskets/master/_listings/request-baskets/basketsname-post-openapi.md
- name: Request Baskets - Update basket settings
  x-api-slug: basketsname-put
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
  image: ""
  humanURL: http://rbaskets.in
  baseURL: https://rbaskets.in//
  tags: Storage, Cache, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/request-baskets/master/_listings/request-baskets/basketsname-put-openapi.md
- name: Request Baskets - Delete all requests
  x-api-slug: basketsnamerequests-delete
  description: Deletes all requests collected by this basket.
  image: ""
  humanURL: http://rbaskets.in
  baseURL: https://rbaskets.in//
  tags: Storage, Cache, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/request-baskets/master/_listings/request-baskets/basketsnamerequests-delete-openapi.md
- name: Request Baskets - Get collected requests
  x-api-slug: basketsnamerequests-get
  description: Fetches collection of requests collected by this basket.
  image: ""
  humanURL: http://rbaskets.in
  baseURL: https://rbaskets.in//
  tags: Storage, Cache, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/request-baskets/master/_listings/request-baskets/basketsnamerequests-get-openapi.md
- name: Request Baskets - Get response settings
  x-api-slug: basketsnameresponsesmethod-get
  description: |-
    Retrieves information about configured response of the basket. Service will reply with this response to any
    HTTP request sent to the basket with appropriate HTTP method.

    If nothing is configured, the default response is HTTP 200 - OK with empty content.
  image: ""
  humanURL: http://rbaskets.in
  baseURL: https://rbaskets.in//
  tags: Storage, Cache, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/request-baskets/master/_listings/request-baskets/basketsnameresponsesmethod-get-openapi.md
- name: Request Baskets - Update response settings
  x-api-slug: basketsnameresponsesmethod-put
  description: |-
    Allows to configure HTTP response of this basket. The service will reply with configured response to any HTTP
    request sent to the basket with appropriate HTTP method.

    If nothing is configured, the default response is HTTP 200 - OK with empty content.
  image: ""
  humanURL: http://rbaskets.in
  baseURL: https://rbaskets.in//
  tags: Storage, Cache, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/request-baskets/master/_listings/request-baskets/basketsnameresponsesmethod-put-openapi.md
x-common:
- type: x-api-gallery
  url: http://regulations.gov.api.gallery.streamdata.io
- type: x-api-stack
  url: http://request.baskets.stack.network
- type: x-website
  url: http://rbaskets.in
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---