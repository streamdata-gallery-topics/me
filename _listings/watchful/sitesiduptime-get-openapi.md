---
swagger: "2.0"
x-collection-name: Watchful
x-complete: 0
info:
  title: Watchful Return Uptime Data
  description: Return uptime data
  version: 1.0.0
host: watchful.li
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /audits/metadata:
    get:
      summary: Get The List Of Fields
      description: Returns a list of fields
      operationId: getFieldsAudits
      x-api-path-slug: auditsmetadata-get
      responses:
        200:
          description: OK
      tags:
      - Audits
      - Metadata
  /extensions/metadata:
    get:
      summary: Get The List Of Fields
      description: Returns a list of fields
      operationId: getFieldsExtensions
      x-api-path-slug: extensionsmetadata-get
      responses:
        200:
          description: OK
      tags:
      - Extensions
      - Metadata
  /feedbacks/metadata:
    get:
      summary: Get The List Of Fields
      description: Returns a list of fields
      operationId: getFieldsFeedbacks
      x-api-path-slug: feedbacksmetadata-get
      responses:
        200:
          description: OK
      tags:
      - Feedbacks
      - Metadata
  /logs/metadata:
    get:
      summary: Get The List Of Fields
      description: Returns a list of fields
      operationId: getFieldsLogs
      x-api-path-slug: logsmetadata-get
      responses:
        200:
          description: OK
      tags:
      - Logs
      - Metadata
  /sites/metadata:
    get:
      summary: Get The List Of Fields
      description: Returns a list of fields
      operationId: sites.metadata.get
      x-api-path-slug: sitesmetadata-get
      responses:
        200:
          description: OK
      tags:
      - Sites
      - Metadata
  /sites/{id}/uptime:
    get:
      summary: Return Uptime Data
      description: Return uptime data
      operationId: getUptime
      x-api-path-slug: sitesiduptime-get
      parameters:
      - in: path
        name: id
        description: ID of the website
      responses:
        200:
          description: OK
      tags:
      - Sites
      - Id
      - Uptime
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