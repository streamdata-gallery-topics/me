---
swagger: "2.0"
x-collection-name: Instructure
x-complete: 0
info:
  title: Instructure Canvas Sections API Get all Peer Reviews
  description: Get all peer reviews.
  termsOfService: https://www.canvaslms.com/policies/api-policy
  version: v1
host: canvas.instructure.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /sections/{course_section_id}/assignments/assignment_id/override:
    get:
      summary: Redirect to the assignment override for a section
      description: Redirect to the assignment override for a section.
      operationId: redirect-to-the-assignment-override-for-a-section
      x-api-path-slug: sectionscourse-section-idassignmentsassignment-idoverride-get
      responses:
        200:
          description: OK
      tags:
      - Sections
      - Course
      - Section
      - Id
      - Assignments
      - Assignment
      - Id
      - Override
  /sections/{section_id}/assignments/assignment_id/peer_reviews:
    get:
      summary: Get all Peer Reviews
      description: Get all peer reviews.
      operationId: get-all-peer-reviews
      x-api-path-slug: sectionssection-idassignmentsassignment-idpeer-reviews-get
      parameters:
      - in: query
        name: include[]
        description: Associations to include with the peer review
      responses:
        200:
          description: OK
      tags:
      - Sections
      - Section
      - Id
      - Assignments
      - Assignment
      - Id
      - Peer
      - Reviews
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