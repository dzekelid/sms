swagger: "2.0"
x-collection-name: Twilio
x-complete: 1
info:
  title: Twilio
  description: twilio-is-a-cloud-communications-infrastructure-as-a-serviceiaas-company-based-in-san-francisco-california--twilio-allows-software-developers-to-programmatically-make-and-receive-phone-calls-and-send-and-receive-text-messages-using-its-web-service-apis--twilios-services-are-accessed-over-http-and-are-billed-based-on-usage-
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
  /Accounts/{AccountSid}/SMS/Messages.{format}:
    get:
      summary: GetSMSList
      description: GetSMSList
      operationId: getsmslist
      x-api-path-slug: accountsaccountsidsmsmessages-format-get
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: format
        description: By default, Twilios REST API returns XML
      responses:
        200:
          description: OK
      tags:
      - SMS Messages
    post:
      summary: SendSMS
      description: SendSMS
      operationId: sendsms
      x-api-path-slug: accountsaccountsidsmsmessages-format-post
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: format
        description: By default, Twilios REST API returns XML
      responses:
        200:
          description: OK
      tags:
      - SMS Messages
  /Accounts/{AccountSid}/SMS/Messages/{SMSMessageSid}.{format}:
    get:
      summary: GetSMS
      description: GetSMS
      operationId: getsms
      x-api-path-slug: accountsaccountsidsmsmessagessmsmessagesid-format-get
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: format
        description: By default, Twilios REST API returns XML
      - in: path
        name: SMSMessageSid
        description: A 34 character string that uniquely identifies the SMS short
          code
      responses:
        200:
          description: OK
      tags:
      - SMS Messages
  /Accounts/{AccountSid}/SMS/ShortCodes:
    get:
      summary: Get SMS Short Code Media
      description: Returns a list of ShortCode resource representations, each representing
        anshort code within your account. The list includes paging information.n
      operationId: returns-a-list-of-shortcode-resource-representations-each-representing-ashort-code-within-your-accou
      x-api-path-slug: accountsaccountsidsmsshortcodes-get
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      responses:
        200:
          description: OK
      tags:
      - Short Codes
  /Accounts/{AccountSid}/SMS/ShortCodes/{ShortCodeSid}:
    get:
      summary: Get SMS Short Code Media
      description: Get a single message.
      operationId: get-a-single-message
      x-api-path-slug: accountsaccountsidsmsshortcodesshortcodesid-get
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: ShortCodeSid
      responses:
        200:
          description: OK
      tags:
      - Short Codes
    post:
      summary: Add SMS Short Code Media
      description: Tries to update the shortcodes properties, and returns the updatednresource
        representation if successful.n
      operationId: tries-to-update-the-shortcodes-properties-and-returns-the-updatedresource-representation-if-successf
      x-api-path-slug: accountsaccountsidsmsshortcodesshortcodesid-post
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: ShortCodeSid
      responses:
        200:
          description: OK
      tags:
      - Short Codes