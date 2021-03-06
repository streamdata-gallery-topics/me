---
name: Pivotal Tracker
x-slug: pivotal-tracker
description: Pivotal Tracker is the agile project management tool of choice for developers
  around the world for real-time collaboration around a shared, prioritized backlog.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11526-pivotal-tracker.jpg
x-kinRank: "7"
x-alexaRank: "15894"
tags: Me
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/pivotal-tracker/apis.md
specificationVersion: "0.14"
apis:
- name: Pivotal Tracker Get Projects Project Memberships
  x-api-slug: pivotal-tracker
  description: Retrieves all memberships for a project.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11526-pivotal-tracker.jpg
  humanURL: http://pivotaltracker.com
  baseURL: https://www.pivotaltracker.com//services/v3///projects/{PROJECT_ID}/memberships
  tags: Projects,PROJECT,ID,Memberships
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/pivotal-tracker/projectsproject-idmemberships-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/pivotal-tracker/projectsproject-idmemberships-get-openapi.md
- name: Pivotal Tracker Post Projects Project Memberships
  x-api-slug: pivotal-tracker
  description: Adds a new membership to a project.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11526-pivotal-tracker.jpg
  humanURL: http://pivotaltracker.com
  baseURL: https://www.pivotaltracker.com//services/v3///projects/{PROJECT_ID}/memberships
  tags: Projects,PROJECT,ID,Memberships
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/pivotal-tracker/projectsproject-idmemberships-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/pivotal-tracker/projectsproject-idmemberships-post-openapi.md
- name: Pivotal Tracker Get Projects Project Memberships Membership
  x-api-slug: pivotal-tracker
  description: Retrieves information about a single membership.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11526-pivotal-tracker.jpg
  humanURL: http://pivotaltracker.com
  baseURL: https://www.pivotaltracker.com//services/v3///projects/{PROJECT_ID}/memberships/{MEMBERSHIP_ID}
  tags: Projects,PROJECT,ID,Memberships,MEMBERSHIP,ID
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/pivotal-tracker/projectsproject-idmembershipsmembership-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/pivotal-tracker/projectsproject-idmembershipsmembership-id-get-openapi.md
- name: Pivotal Tracker Delete Projects Project Memberships Membership
  x-api-slug: pivotal-tracker
  description: Delete projects project memberships membership.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11526-pivotal-tracker.jpg
  humanURL: http://pivotaltracker.com
  baseURL: https://www.pivotaltracker.com//services/v3///projects/{PROJECT_ID}/memberships/{MEMBERSHIP_ID}
  tags: Projects,PROJECT,ID,Memberships,MEMBERSHIP,ID
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/pivotal-tracker/projectsproject-idmembershipsmembership-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/pivotal-tracker/projectsproject-idmembershipsmembership-id-delete-openapi.md
- name: Pivotal Tracker Post Projects Project Stories Story Attachments
  x-api-slug: pivotal-tracker
  description: Post projects project stories story attachments.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11526-pivotal-tracker.jpg
  humanURL: http://pivotaltracker.com
  baseURL: https://www.pivotaltracker.com//services/v3///projects/{PROJECT_ID}/stories/{STORY_ID}/attachments
  tags: Projects,PROJECT,ID,Stories,STORY,ID,Attachments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/pivotal-tracker/projectsproject-idstoriesstory-idattachments-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/pivotal-tracker/projectsproject-idstoriesstory-idattachments-post-openapi.md
- name: Pivotal Tracker
  x-api-slug: pivotal-tracker
  description: Whether welding together two apps or forging a unique one, tap into
    100% of the Tracker feature set with the very same API the Tracker team uses.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/11526-pivotal-tracker.jpg
  humanURL: http://pivotaltracker.com
  baseURL: https://www.pivotaltracker.com//services/v3/
  tags: Me
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/pivotal-tracker/openapi.md
x-common:
- type: x-blog
  url: http://www.pivotaltracker.com/community/tracker-blog
- type: x-blog
  url: http://www.pivotaltracker.com/feed
- type: x-crunchbase
  url: https://crunchbase.com/organization/pivotaltracker
- type: x-email
  url: TRACKER@PIVOTAL.IO
- type: x-faq
  url: https://www.pivotaltracker.com/faq
- type: x-github
  url: https://github.com/pivotal
- type: x-linkedin
  url: https://www.linkedin.com/showcase/pivotal-tracker/
- type: x-pricing
  url: http://www.pivotaltracker.com/why-tracker/pricing
- type: x-selfservice-registration
  url: https://www.pivotaltracker.com/signup/new
- type: x-status
  url: http://status.pivotaltracker.com/
- type: x-terms-of-service
  url: https://www.pivotaltracker.com/policy/eula
- type: x-twitter
  url: https://twitter.com/pivotaltracker
- type: x-website
  url: http://pivotaltracker.com
- type: x-website
  url: http://www.pivotaltracker.com/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---