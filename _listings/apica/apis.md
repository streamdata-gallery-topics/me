---
name: Apica
x-slug: apica
description: Apicas performance testing and monitoring solutions provide critical
  peak performance data and 24/7 monitoring of applications and sites around the world.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19004-apica.jpg
x-kinRank: "7"
x-alexaRank: "876355"
tags: Me
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/apica/apis.md
specificationVersion: "0.14"
apis:
- name: Customers API Customers {customerId}
  x-api-slug: customers-api
  description: Returns subcustomer by subcustomer's ID.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19004-apica.jpg
  humanURL: https://www.apicasystem.com
  baseURL: '://///customers/{customerId} '
  tags: Customers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/apica/customerscustomerid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/apica/customerscustomerid-get-openapi.md
- name: Customers API Customers
  x-api-slug: customers-api
  description: Creates customer.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19004-apica.jpg
  humanURL: https://www.apicasystem.com
  baseURL: '://///customers '
  tags: Customers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/apica/customers-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/apica/customers-post-openapi.md
- name: Customers API Customers {customerId} Subscription
  x-api-slug: customers-api
  description: Updates customer's subscription.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19004-apica.jpg
  humanURL: https://www.apicasystem.com
  baseURL: '://///customers/{customerId}/subscription '
  tags: Customers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/apica/customerscustomeridsubscription-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/apica/customerscustomeridsubscription-put-openapi.md
- name: Customers API
  x-api-slug: customers-api
  description: Apicas performance testing and monitoring solutions provide critical
    peak performance data and 24/7 monitoring of applications and sites around the
    world.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19004-apica.jpg
  humanURL: https://www.apicasystem.com
  baseURL: :///
  tags: Me
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/apica/openapi.md
- name: Messages API Clear a bucket (remove all messages).
  x-api-slug: messages-api
  description: Clear a bucket (remove all messages)..
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19004-apica.jpg
  humanURL: https://www.apicasystem.com
  baseURL: ://///buckets/{bucketKey}/messages
  tags: Buckets,BucketKey,Messages
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/apica/bucketsbucketkeymessages-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/apica/bucketsbucketkeymessages-delete-openapi.md
- name: Messages API Retrieve a list of messages in a bucket
  x-api-slug: messages-api
  description: Retrieve a list of messages in a bucket.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19004-apica.jpg
  humanURL: https://www.apicasystem.com
  baseURL: ://///buckets/{bucketKey}/messages
  tags: Buckets,BucketKey,Messages
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/apica/bucketsbucketkeymessages-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/apica/bucketsbucketkeymessages-get-openapi.md
- name: Messages API Create a message
  x-api-slug: messages-api
  description: Create a message.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19004-apica.jpg
  humanURL: https://www.apicasystem.com
  baseURL: ://///buckets/{bucketKey}/messages
  tags: Buckets,BucketKey,Messages
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/apica/bucketsbucketkeymessages-post-openapi.md
- name: Messages API Retrieve the details for a single message.
  x-api-slug: messages-api
  description: Retrieve the details for a single message..
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19004-apica.jpg
  humanURL: https://www.apicasystem.com
  baseURL: ://///buckets/{bucketKey}/messages/{messageId}
  tags: Buckets,BucketKey,Messages,MessageId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/apica/bucketsbucketkeymessagesmessageid-get-openapi.md
- name: Messages API Messages?active={active}&amp;customerId={customerId}
  x-api-slug: messages-api
  description: Gets a list of UI messages. UI messages are used for user notifications
    on announcements/information/warnings.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19004-apica.jpg
  humanURL: https://www.apicasystem.com
  baseURL: '://///messages?active={active}&amp;customerId={customerId} '
  tags: Messages?active=active&amp;customerId=customerId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/apica/messagesactiveactiveampcustomeridcustomerid-get-openapi.md
- name: Messages API Messages
  x-api-slug: messages-api
  description: Creates an UI message.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19004-apica.jpg
  humanURL: https://www.apicasystem.com
  baseURL: '://///messages '
  tags: Messages
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/apica/messages-post-openapi.md
- name: Messages API Messages {id}
  x-api-slug: messages-api
  description: Gets an existing UI message by Id.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19004-apica.jpg
  humanURL: https://www.apicasystem.com
  baseURL: '://///messages/{id} '
  tags: Messages,Id
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/apica/messagesid-get-openapi.md
- name: Messages API Messages {id}
  x-api-slug: messages-api
  description: Updates an existing UI message.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19004-apica.jpg
  humanURL: https://www.apicasystem.com
  baseURL: '://///messages/{id} '
  tags: Messages,Id
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/apica/messagesid-put-openapi.md
- name: Messages API Messages {id}
  x-api-slug: messages-api
  description: Deletes an existing UI message.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19004-apica.jpg
  humanURL: https://www.apicasystem.com
  baseURL: '://///messages/{id} '
  tags: Messages,Id
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/apica/messagesid-delete-openapi.md
- name: Messages API
  x-api-slug: messages-api
  description: Apicas performance testing and monitoring solutions provide critical
    peak performance data and 24/7 monitoring of applications and sites around the
    world.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19004-apica.jpg
  humanURL: https://www.apicasystem.com
  baseURL: :///
  tags: Me
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/apica/openapi.md
x-common:
- type: x-blog
  url: https://www.apicasystem.com/blog/
- type: x-blog-rss
  url: https://www.apicasystem.com/feed/
- type: x-crunchbase
  url: https://crunchbase.com/organization/apica
- type: x-developer
  url: http://api-wpm.apicasystem.com/v3/help
- type: x-documentation
  url: https://api-wpm.apicasystem.com/v3/Help
- type: x-email
  url: support@apicasystems.com
- type: x-email
  url: sales@apicasystems.com
- type: x-email
  url: swesales@apicasystems.com
- type: x-email
  url: operations@apicasystem.com
- type: x-github
  url: https://github.com/ApicaSystem
- type: x-linkedin
  url: https://www.linkedin.com/company/apica-ab
- type: x-phone
  url: 1 (310) 776-7540
- type: x-twitter
  url: https://twitter.com/apicasystems
- type: x-website
  url: https://www.apicasystem.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---