---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Returns a list of sms templates associated to this agency
  version: 1.0.0
  description: Returns a list of sms templates associated to this agency.
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/branding/uploadsmstemplate:
    post:
      summary: Upload the data to create a SMS Document Template for a Brand.
      description: Upload the data to create a sms document template for a brand..
      operationId: Branding_UploadSMSTemplateBybrandTemplateSaveDataContract
      x-api-path-slug: apibrandinguploadsmstemplate-post
      parameters:
      - in: body
        name: brandTemplateSaveDataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Upload
      - Data
      - To
      - Create
      - SMS
      - Document
      - Templatea
      - Brand
  /api/documentgeneration/smstemplates:
    get:
      summary: Returns a list of sms templates associated to this agency
      description: Returns a list of sms templates associated to this agency.
      operationId: DocumentGeneration_GetSmsTemplates
      x-api-path-slug: apidocumentgenerationsmstemplates-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Returns
      - List
      - Of
      - Sms
      - Templates
      - Associated
      - To
      - This
      - Agency
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