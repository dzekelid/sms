---
swagger: "2.0"
x-collection-name: AT&T Dev Program
x-complete: 0
info:
  title: AT&T API Get SMS Messaging Outbox Messageid
  description: /sms/v3/messaging/outbox/{messageId}
  version: "1"
host: api.att.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /sms/v3/messaging/inbox/{RegistrationID}:
    get:
      summary: Get SMS Messaging Inbox Registration
      description: /sms/v3/messaging/inbox/{RegistrationID}
      operationId: smsv3messaginginboxregistrationid
      x-api-path-slug: smsv3messaginginboxregistrationid-get
      parameters:
      - in: path
        name: RegistrationID
      responses:
        200:
          description: OK
      tags:
      - Sms
      - VMessaging
      - Inbox
      - RegistrationID
  /sms/v3/messaging/outbox:
    post:
      summary: Post SMS Messaging Outbox
      description: /sms/v3/messaging/outbox
      operationId: smsv3messagingoutbox
      x-api-path-slug: smsv3messagingoutbox-post
      responses:
        200:
          description: OK
      tags:
      - Sms
      - VMessaging
      - Outbox
  /sms/v3/messaging/outbox/{messageId}:
    get:
      summary: Get SMS Messaging Outbox Messageid
      description: /sms/v3/messaging/outbox/{messageId}
      operationId: smsv3messagingoutboxmessageid
      x-api-path-slug: smsv3messagingoutboxmessageid-get
      parameters:
      - in: path
        name: messageId
      responses:
        200:
          description: OK
      tags:
      - Sms
      - VMessaging
      - Outbox
      - MessageId
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