---
swagger: "2.0"
x-collection-name: Transport for London Unified
x-complete: 0
info:
  title: Transport for London Unified Stop Point  Sms
  description: Gets a stoppoint for a given sms code..
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