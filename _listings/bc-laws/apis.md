---
name: BC Laws
x-slug: bc-laws
description: 'BC Laws is an electronic library providing free public access to the
  laws of British Columbia. BC Laws is hosted by the Queen&rsquo;s Printer of British
  Columbia and published in partnership with the Ministry of Justice and the Law Clerk
  of the Legislative Assembly. BC Laws contains a comprehensive collection of BC legislation
  and related materials. It is available on the internet in two forms: First: The
  library is available as a web site in which users can browse and search the laws
  of British Columbia. Second: The library is available as a portal to legislation
  in raw XML1 data format, accessible via the BC Laws API2. This direct access to
  raw data is intended to enable third parties to build or add their own custom applications
  based on the structure of the data and all the associated search functionality inherent
  in that structure. The BC Laws website itself is an example of one such application.'
image: ""
x-kinRank: "7"
x-alexaRank: "0"
tags: Me
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/bc-laws/apis.md
specificationVersion: "0.14"
apis:
- name: BC Laws Lists the metadata available for the specified index or directory
    from the BCLaws legislative respository
  x-api-slug: bc-laws
  description: Lists the metadata available for the specified index or directory from
    the BCLaws legislative respository
  image: ""
  humanURL: http://bclaws.ca
  baseURL: https://www.bclaws.ca//civix//content/{aspectId}/{civixDocumentId}
  tags: Content,AspectId,CivixDocumentId
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/bc-laws/contentaspectidcivixdocumentid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/bc-laws/contentaspectidcivixdocumentid-get-openapi.md
- name: BC Laws Retrieves a specific document from the BCLaws legislative repository
    (HTML format)
  x-api-slug: bc-laws
  description: 'The /document API allows you to retrieve actual documents from the
    BCLaws legislative repository. To retrieve a document from the repository you
    need the aspect identifier and two other specific pieces of information about
    the document: the index identifier and the document identifier. These unique identifiers
    can be retrieved from the /content API.'
  image: ""
  humanURL: http://bclaws.ca
  baseURL: https://www.bclaws.ca//civix//document/id/{aspectId}/{civixIndexId}/{civixDocumentId}
  tags: Document,Id,AspectId,CivixIndexId,CivixDocumentId
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/bc-laws/documentidaspectidcivixindexidcivixdocumentid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/bc-laws/documentidaspectidcivixindexidcivixdocumentid-get-openapi.md
- name: BC Laws Retrieves a specific document from the BCLaws legislative repository
    with search text highlighted (HTML format)
  x-api-slug: bc-laws
  description: 'The /document API allows you to retrieve actual documents from the
    BCLaws legislative repository. To retrieve a document from the repository you
    need the aspect identifier and two other specific pieces of information about
    the document: the index identifier and the document identifier. These unique identifiers
    can be retrieved from the /content API.'
  image: ""
  humanURL: http://bclaws.ca
  baseURL: https://www.bclaws.ca//civix//document/id/{aspectId}/{civixIndexId}/{civixDocumentId}/search/{searchString}
  tags: Document,Id,AspectId,CivixIndexId,CivixDocumentId,Search,SearchString
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/bc-laws/documentidaspectidcivixindexidcivixdocumentidsearchsearchstring-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/bc-laws/documentidaspectidcivixindexidcivixdocumentidsearchsearchstring-get-openapi.md
- name: BC Laws Retrieves a specific document from the BCLaws legislative repository
    (XML format)
  x-api-slug: bc-laws
  description: 'The /document API allows you to retrieve actual documents from the
    BCLaws legislative repository. To retrieve a document from the repository you
    need the aspect identifier and two other specific pieces of information about
    the document: the index identifier and the document identifier. These unique identifiers
    can be retrieved from the /content API.'
  image: ""
  humanURL: http://bclaws.ca
  baseURL: https://www.bclaws.ca//civix//document/id/{aspectId}/{civixIndexId}/{civixDocumentId}/xml
  tags: Document,Id,AspectId,CivixIndexId,CivixDocumentId,Xml
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/bc-laws/documentidaspectidcivixindexidcivixdocumentidxml-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/bc-laws/documentidaspectidcivixindexidcivixdocumentidxml-get-openapi.md
- name: BC Laws Retrieves a specific document from the BCLaws legislative repository
    with search text highlighted (XML format)
  x-api-slug: bc-laws
  description: 'The /document API allows you to retrieve actual documents from the
    BCLaws legislative repository. To retrieve a document from the repository you
    need the aspect identifier and two other specific pieces of information about
    the document: the index identifier and the document identifier. These unique identifiers
    can be retrieved from the /content API.'
  image: ""
  humanURL: http://bclaws.ca
  baseURL: https://www.bclaws.ca//civix//document/id/{aspectId}/{civixIndexId}/{civixDocumentId}/xml/search/{searchString}
  tags: Document,Id,AspectId,CivixIndexId,CivixDocumentId,Xml,Search,SearchString
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/bc-laws/documentidaspectidcivixindexidcivixdocumentidxmlsearchsearchstring-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/bc-laws/documentidaspectidcivixindexidcivixdocumentidxmlsearchsearchstring-get-openapi.md
- name: BC Laws
  x-api-slug: bc-laws
  description: 'BC Laws is an electronic library providing free public access to the
    laws of British Columbia. BC Laws is hosted by the Queen&rsquo;s Printer of British
    Columbia and published in partnership with the Ministry of Justice and the Law
    Clerk of the Legislative Assembly. BC Laws contains a comprehensive collection
    of BC legislation and related materials. It is available on the internet in two
    forms: First: The library is available as a web site in which users can browse
    and search the laws of British Columbia. Second: The library is available as a
    portal to legislation in raw XML1 data format, accessible via the BC Laws API2.
    This direct access to raw data is intended to enable third parties to build or
    add their own custom applications based on the structure of the data and all the
    associated search functionality inherent in that structure. The BC Laws website
    itself is an example of one such application.'
  image: ""
  humanURL: http://bclaws.ca
  baseURL: https://www.bclaws.ca//civix
  tags: Me
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/me/master/_listings/bc-laws/openapi.md
x-common:
- type: x-website
  url: http://bclaws.ca
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---