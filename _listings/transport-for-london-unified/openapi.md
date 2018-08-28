swagger: "2.0"
x-collection-name: Transport for London Unified
x-complete: 1
info:
  title: Transport for London Unified
  description: our-unified-api-brings-together-data-across-all-modes-of-transport-into-a-single-restful-api--this-api-provides-access-to-the-most-highly-requested-realtime-and-status-infomation-across-all-the-modes-of-transport-in-a-single-and-consistent-way--access-to-the-developer-documentation-is-available-at-httpsapi-tfl-gov-uk
  version: v1
host: api.tfl.gov.uk
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /StopPoint/Sms/{id}:
    get:
      summary: Stop Point  Sms
      description: Gets a stoppoint for a given sms code..
      operationId: StopPoint_GetBySms
      x-api-path-slug: stoppointsmsid-get
      parameters:
      - in: path
        name: id
        description: A 5-digit Countdown Bus Stop Code e
      - in: query
        name: output
        description: If set to web, a 302 redirect to relevant website bus stop page
          is returned
      responses:
        200:
          description: OK
      tags:
      - Stop
      - Point
      - ""
      - Sms