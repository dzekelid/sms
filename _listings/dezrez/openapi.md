swagger: "2.0"
x-collection-name: Dezrez
x-complete: 1
info:
  title: Dezrez.Rezi.Client.Api
  version: 1.0.0
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
  /api/group/{id}/sendsms:
    post:
      summary: To send an adhoc sms to a group
      description: To send an adhoc sms to a group.
      operationId: Group_SendSMSByidBysmsDataContract
      x-api-path-slug: apigroupidsendsms-post
      parameters:
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: body
        name: smsDataContract
        description: Details of the sms to send
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - To
      - Send
      - Adhoc
      - Sms
      - To
      - Group