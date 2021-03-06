---
swagger: "2.0"
x-collection-name: Twilio
x-complete: 0
info:
  title: Twilio Get Message Media
  description: Without an extension, the media is returned using the mime-type provided
    when the media was generated.
  termsOfService: https://www.twilio.com/legal/tos
  version: v1
host: api.twilio.com
basePath: /2010-04-01/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Accounts/{AccountSid}/Messages/{MessageSid}/Media/{MediaSid}:
    get:
      summary: Get Message Media
      description: Without an extension, the media is returned using the mime-type
        provided when the media was generated.
      operationId: without-an-extension-the-media-is-returned-using-the-mimetype-provided-when-the-media-was-generated
      x-api-path-slug: accountsaccountsidmessagesmessagesidmediamediasid-get
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: MediaSid
        description: A 34 character string that uniquely identifies the media object
      - in: path
        name: MessageSid
        description: A 34 character string that uniquely identifies the message
      responses:
        200:
          description: OK
      tags:
      - Messages
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