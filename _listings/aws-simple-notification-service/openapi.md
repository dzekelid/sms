swagger: "2.0"
x-collection-name: AWS Simple Notification Service
x-complete: 1
info:
  title: AWS Simple Notification Service API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=GetSMSAttributes:
    get:
      summary: Get S M S Attributes
      description: Returns the settings for sending SMS messages from your account.
      operationId: getSMSAttributes
      x-api-path-slug: actiongetsmsattributes-get
      parameters:
      - in: query
        name: attributes.member.N
        description: A list of the individual attribute names, such as MonthlySpendLimit,
          for which      you want values
        type: string
      responses:
        200:
          description: OK
      tags:
      - SMS
  /?Action=SetSMSAttributes:
    get:
      summary: Set SMS Attributes
      description: Use this request to set the default settings for sending SMS messages
        and receiving daily SMS usage reports.
      operationId: setSMSAttributes
      x-api-path-slug: actionsetsmsattributes-get
      parameters:
      - in: query
        name: |-
          attributes
                      , attributes.entry.N.key (key), attributesentry.N.value (value)
        description: The default settings for sending SMS messages from your account
        type: string
      responses:
        200:
          description: OK
      tags:
      - SMS
  /?Action=CheckIfPhoneNumberIsOptedOut:
    get:
      summary: Check If Phone Number Is Opted Out
      description: Accepts a phone number and indicates whether the phone holder has
        opted out of receiving SMS messages from your account.
      operationId: checkIfPhoneNumberIsOptedOut
      x-api-path-slug: actioncheckifphonenumberisoptedout-get
      parameters:
      - in: query
        name: phoneNumber
        description: The phone number for which you want to check the opt out status
        type: string
      responses:
        200:
          description: OK
      tags:
      - Opt Out
  /?Action=ListPhoneNumbersOptedOut:
    get:
      summary: List Phone Numbers Opted Out
      description: Returns a list of phone numbers that are opted out, meaning you
        cannot send SMS messages to them.
      operationId: listPhoneNumbersOptedOut
      x-api-path-slug: actionlistphonenumbersoptedout-get
      parameters:
      - in: query
        name: nextToken
        description: A NextToken string is used when you call the      ListPhoneNumbersOptedOut
          action to retrieve additional records that are      available after the
          first page of results
        type: string
      responses:
        200:
          description: OK
      tags:
      - Opt Out
  /?Action=OptInPhoneNumber:
    get:
      summary: Opt In Phone Number
      description: Use this request to opt in a phone number that is opted out, which
        enables you to resume sending SMS messages to the number.
      operationId: optInPhoneNumber
      x-api-path-slug: actionoptinphonenumber-get
      parameters:
      - in: query
        name: phoneNumber
        description: The phone number to opt in
        type: string
      responses:
        200:
          description: OK
      tags:
      - Opt Out