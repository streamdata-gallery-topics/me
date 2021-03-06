---
swagger: "2.0"
x-collection-name: Bitly
x-complete: 1
info:
  title: Bitly Organization Metric API
  description: the-bitly-organization-metric-api
  termsOfService: http://dev.bitly.com/best_practices.html
  version: v3
host: api-ssl.bitly.com
basePath: /v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/organization/brand_messages:
    get:
      summary: Organization Brand Messages
      description: Returns the top Bitlinks created by you with traffic, that did
        not also have non-organization traffic in the same time period, ordered by
        clicks.
      operationId: organizationBrandMessages
      x-api-path-slug: v3organizationbrand-messages-get
      parameters:
      - in: query
        name: domain
        description: a tracking or e2e domain for this organization
      - in: query
        name: limit
        description: "1"
      - in: query
        name: timezone
        description: an integer hour offset from UTC (-14
      - in: query
        name: unit
        description: hour | day | week | month default:day
      - in: query
        name: units
        description: an integer representing the time units to query data for
      - in: query
        name: unit_reference_ts
        description: an epoch timestamp, indicating the most recent time for which
          to pull metrics
      responses:
        200:
          description: OK
      tags:
      - Organization
      - Brand
      - Messages
---