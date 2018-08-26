---
name: Request Baskets
x-slug: request-baskets
description: ""
image: ""
x-kinRank: "7"
x-alexaRank: "0"
tags: Request Baskets
created: "2018-08-26"
modified: "2018-08-26"
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