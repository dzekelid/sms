swagger: "2.0"
x-collection-name: AWS Cognito
x-complete: 1
info:
  title: AWS Cognito Merged API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AdminCreateUser:
    get:
      summary: Admin Create User
      description: |-
        Creates a new user in the specified user pool and sends a welcome message via email
                    or phone (SMS).
      operationId: adminCreateUser
      x-api-path-slug: actionadmincreateuser-get
      parameters:
      - in: query
        name: DesiredDeliveryMediums
        description: Specify EMAIL if email will be used to send the welcome message
        type: string
      - in: query
        name: ForceAliasCreation
        description: This parameter is only used if the phone_number_verified or email_verified            attribute
          is set to True
        type: string
      - in: query
        name: MessageAction
        description: Set to RESEND to resend the invitation message to a user that
          already exists and            reset the expiration limit on the users account
        type: string
      - in: query
        name: TemporaryPassword
        description: The users temporary password
        type: string
      - in: query
        name: UserAttributes
        description: An array of name-value pairs that contain user attributes and
          attribute values to            be set for the user to be created
        type: string
      - in: query
        name: Username
        description: The username for the user
        type: string
      - in: query
        name: UserPoolId
        description: The user pool ID for the user pool where the user will be created
        type: string
      - in: query
        name: ValidationData
        description: The users validation data
        type: string
      responses:
        200:
          description: OK
      tags:
      - Users