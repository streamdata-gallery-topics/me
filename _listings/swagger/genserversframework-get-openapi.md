---
swagger: "2.0"
x-collection-name: Swagger
x-complete: 0
info:
  title: Swagger Generator Returns options for a server framework
  description: Returns options for a server framework.
  termsOfService: http://swagger.io/terms/
  contact:
    name: apiteam@swagger.io
  version: 2.2.3
host: generator.swagger.io
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /gen/servers/{framework}:
    get:
      summary: Returns options for a server framework
      description: Returns options for a server framework.
      operationId: getServerOptions
      x-api-path-slug: genserversframework-get
      parameters:
      - in: path
        name: framework
        description: The target language for the server framework
      responses:
        200:
          description: OK
      tags:
      - Generate
      - Servers
      - Framework
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