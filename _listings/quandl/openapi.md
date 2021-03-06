---
swagger: "2.0"
x-collection-name: Quandl
x-complete: 1
info:
  title: Quandl
  description: the-quandl-api
  version: 1.0.0
host: www.quandl.com
basePath: /api/v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /datasets/{database_code}/{dataset_code}/metadata:
    get:
      summary: Get Datasets Database Code Dataset Code Metadata
      description: 'To download the metadata associated with any dataset object, append
        /metadata to your API request. (You can replace .csv with .json or .xml in
        this request). The following metadata fields are available in the response:'
      operationId: datasets.database_code.dataset_code.metadata.get
      x-api-path-slug: datasetsdatabase-codedataset-codemetadata-get
      parameters:
      - in: query
        name: column_names
      - in: path
        name: database_code
        description: The unique database code on Quandl (ex
      - in: path
        name: dataset_code
        description: The unique dataset code on Quandl (ex
      - in: query
        name: description
      - in: query
        name: frequency
      - in: query
        name: name
      - in: query
        name: newest_available_date
      - in: query
        name: oldest_available_date
      - in: query
        name: premium
      - in: query
        name: refreshed_at
      - in: query
        name: type
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Datasets
      - Database
      - Code
      - Dataset
      - Code
      - Metadata
---