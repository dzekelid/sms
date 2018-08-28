swagger: "2.0"
x-collection-name: RingCentral
x-complete: 1
info:
  title: RingCentral Connect Platform API Explorer
  description: this-is-an-interactive-api-explorer-for-the-ringcentral-connect-platform--to-use-this-service-you-will-need-to-have-a-developer-account---links--a-hrefhttpsnetstorage-ringcentral-comdpwapiexplorerrcplatform-basic-ymlv20180514092722-target-blankringcentral-api-specaspannbspnbspopenapi-fka-swagger-formatnbspnbspnbspnbspspana-hrefhttpsgithub-comoaiopenapispecification-target-blanklearn-more-about-openapia
  version: 1.0.0
host: platform.ringcentral.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /restapi/v1.0/account/{accountId}/extension/{extensionId}/sms:
    post:
      summary: Create SMS Message
      description: "Creates and sends new SMS message. Sending SMS messages simultaneously
        to different recipients is limited up to 50 requests per minute; relevant
        for all client applications.\nApp Permission\nSMS\nUser Permission\nOutboundSMS\nUsage
        Plan Group\nMedium\nError Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error
        Message\n   \n \n\n400\nCMN-101\nParameter [] value is invalid\n\n\n400\nCMN-406\nDuplicate
        value for parameter to: +13476733173 found in request\n\n\n400\nMSG-243\nParameter
        [to] value [18882049692] is invalid [Phone number is blocked]\n\n\n400\nMSG-245\nParameter
        [from] value [88121002330] is invalid [Cannot find the phone number which
        belongs to user]\n\n\n400\nMSG-246\nSending SMS from/to extension numbers
        is not available\n\n\n400\nMSG-247\nSending SMS to short numbers is not available\n\n\n400\nMSG-365\nParameters
        [country.id] and [country.isoCode] can not be specified simultaneously\n\n\n400\nMSG-376\nAttachment
        size limit exceeded\n\n\n400\nMSG-379\nToo many attachments\n\n\n400\nMSG-381\nExceeded
        maximum number of recipients for a Group MMS: [10]\n\n\n403\nBIL-103\nFeature
        [MMS] is not available for current account\n\n\n403\nCMN-401\nIn order to
        call this API endpoint, application needs to have [SMS] permission\n\n\n403\nCMN-408\nIn
        order to call this API endpoint, user needs to have [OutboundSMS] permission
        for requested resource.\n\n\n403\nMSG-240\nInternational SMS is not available
        for account.\n\n\n403\nMSG-241\nCannot send SMS from Fax number\n\n\n403\nMSG-242\nThe
        requested feature is not available\n\n\n403\nMSG-314\nExtension is of inappropriate
        type\n\n\n403\nMSG-367\n\"from\" phone number does not support SMS\n\n\n403\nMSG-383\nInternational
        MMS feature is not available\n\n\n403\nMSG-384\nAccount limits exceeded. Cannot
        send the message.\n\n\n403\nMSG-388\nThe destination is prohibited\n\n\n404\nCMN-102\nResource
        for parameter [accountId] is not found\n\n\n415\nMSG-348\nUnsupported attachment
        media type, attachment [3]: [stuff.smil]"
      operationId: sendSMS
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidsms-post
      parameters:
      - in: path
        name: accountId
        description: Internal identifier of a RingCentral account or tilde (~) to
          indicate the account logged-in within the current session
      - in: body
        name: body
        description: JSON body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: extensionId
        description: Internal identifier of an extension or tilde (~) to indicate
          the extension assigned to the account logged-in within the current session
      responses:
        200:
          description: OK
      tags:
      - SMS
      - Message