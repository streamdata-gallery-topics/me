---
swagger: "2.0"
x-collection-name: Flat
x-complete: 0
info:
  title: Flat List comments
  description: This method lists the different comments added on a music score (documents
    and inline) sorted by their post dates.
  termsOfService: https://flat.io/legal
  contact:
    name: Flat
    url: https://flat.io/support
    email: developers@flat.io
  version: 2.1.0
host: api.flat.io
basePath: /v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /scores/{score}:
    get:
      summary: Get a score's metadata
      description: |-
        Get the details of a score identified by the `score` parameter in the URL.
        The currently authenticated user must have at least a read access to the document to use this API call.
      operationId: getScore
      x-api-path-slug: scoresscore-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Scores
      - Metadata
    put:
      summary: Edit a score's metadata
      description: |-
        This API method allows you to change the metadata of a score document (e.g. its `title` or `privacy`), all the properties are optional.

        To edit the file itself, create a new revision using the appropriate method (`POST /v2/scores/{score}/revisions/{revision}`).
      operationId: editScore
      x-api-path-slug: scoresscore-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Edit
      - Scores
      - Metadata
  /scores/{score}/comments:
    get:
      summary: List comments
      description: This method lists the different comments added on a music score
        (documents and inline) sorted by their post dates.
      operationId: getScoreComments
      x-api-path-slug: scoresscorecomments-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - List
      - Comments
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