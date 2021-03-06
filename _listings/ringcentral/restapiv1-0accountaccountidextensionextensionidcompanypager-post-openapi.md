---
swagger: "2.0"
x-collection-name: RingCentral
x-complete: 0
info:
  title: RingCentral Create Pager Message
  description: "Creates and sends a pager message.\nApp Permission\nInternalMessages\nUser
    Permission\nInternalSMS\nUsage Plan Group\nMedium\nError Codes\n\n \n  \n   HTTP
    Code\n   Error Code\n   Error Message\n   \n \n\n400\nCMN-101\nParameter [to.phoneNumber]
    value is invalid\n\n\n400\nCMN-102\nResource for parameter [to] is not found\n\n\n400\nMSG-316\nParameter
    [to] value [102] is invalid [Target extension not found]\n\n\n400\nMSG-324\nExtension
    is of unappropriate state\n\n\n400\nMSG-331\nParameter [from] value [11111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111]
    is invalid [Sender extension number does not correspond to logged in extension]\n\n\n400\nMSG-332\nParameter
    [from] value [404544780008] is invalid [Sender extension id does not correspond
    to logged in extension]\n\n\n400\nMSG-335\nRecipient extension number does not
    correspond to ID\n\n\n403\nCMN-401\nIn order to call this API endpoint, application
    needs to have [InternalMessages] permission\n\n\n403\nCMN-408\nIn order to call
    this API endpoint, user needs to have [InternalSMS] permission for requested resource.\n\n\n403\nMSG-325\nReply
    is forbidden for old message threads\n\n\n403\nMSG-326\nReply is denied for user,
    who is no longer a thread participant\n\n\n403\nMSG-330\nSender extension is of
    unappropriate type\n\n\n404\nCMN-102\nResource for parameter [extensionId] is
    not found"
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
  /restapi/v1.0/account/{accountId}/extension/{extensionId}/company-pager:
    post:
      summary: Create Pager Message
      description: "Creates and sends a pager message.\nApp Permission\nInternalMessages\nUser
        Permission\nInternalSMS\nUsage Plan Group\nMedium\nError Codes\n\n \n  \n
        \  HTTP Code\n   Error Code\n   Error Message\n   \n \n\n400\nCMN-101\nParameter
        [to.phoneNumber] value is invalid\n\n\n400\nCMN-102\nResource for parameter
        [to] is not found\n\n\n400\nMSG-316\nParameter [to] value [102] is invalid
        [Target extension not found]\n\n\n400\nMSG-324\nExtension is of unappropriate
        state\n\n\n400\nMSG-331\nParameter [from] value [11111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111]
        is invalid [Sender extension number does not correspond to logged in extension]\n\n\n400\nMSG-332\nParameter
        [from] value [404544780008] is invalid [Sender extension id does not correspond
        to logged in extension]\n\n\n400\nMSG-335\nRecipient extension number does
        not correspond to ID\n\n\n403\nCMN-401\nIn order to call this API endpoint,
        application needs to have [InternalMessages] permission\n\n\n403\nCMN-408\nIn
        order to call this API endpoint, user needs to have [InternalSMS] permission
        for requested resource.\n\n\n403\nMSG-325\nReply is forbidden for old message
        threads\n\n\n403\nMSG-326\nReply is denied for user, who is no longer a thread
        participant\n\n\n403\nMSG-330\nSender extension is of unappropriate type\n\n\n404\nCMN-102\nResource
        for parameter [extensionId] is not found"
      operationId: sendInternalMessage
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidcompanypager-post
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
      - Pager
      - Message
  /restapi/v1.0/account/{accountId}/extension/{extensionId}/fax:
    post:
      summary: Create Fax Message
      description: "Creates and sends/resends new fax message. Resend can be done
        if sending failed.\nApp Permission\nFaxes\nUser Permission\nOutboundFaxes\nUsage
        Plan Group\nHeavy\nError Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error
        Message\n   \n \n\n400\nCMN-101\nParameter [to] value is invalid\n\n\n400\nMSG-344\nSending
        fax to extension numbers is not available\n\n\n400\nMSG-347\nAttachment [t.txt]
        body is empty\n\n\n400\nMSG-355\nFor binary data filename with extension should
        be specified, attachment [1]: []\n\n\n400\nMSG-356\nEither filename or content
        type should be specified, attachment [1]: []\n\n\n400\nMSG-365\nParameters
        [country.id] and [country.isoCode] can not be specified simultaneously\n\n\n400\nMSG-370\nfilename
        is too long, 256 characters allowed\n\n\n403\nCMN-401\nIn order to call this
        API endpoint, application needs to have [Faxes] permission\n\n\n403\nCMN-408\nIn
        order to call this API endpoint, user needs to have [OutboundFaxes] permission
        for requested resource.\n\n\n404\nCMN-102\nResource for parameter [extensionId]
        is not found\n\n\n415\nMSG-348\nUnsupported attachment media type, attachment
        [1]: [.jfif]\n\n\n415\nMSG-353\nNo file extension or content type specified,
        attachment [1]: [filename,txt]"
      operationId: sendFaxMessage
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidfax-post
      parameters:
      - in: path
        name: accountId
        description: Internal identifier of a RingCentral account (integer) or tilde
          (~) to indicate the account which was logged-in within the current session
      - in: formData
        name: attachment
        description: File to upload
      - in: formData
        name: coverIndex
        description: Cover page identifier
      - in: formData
        name: coverPageText
        description: Cover page text, entered by the fax sender and printed on the
          cover page
      - in: path
        name: extensionId
        description: Internal identifier of an extension (integer) or tilde (~) to
          indicate the extension assigned to the account logged-in within the current
          session
      - in: formData
        name: faxResolution
        description: Resolution of Fax
      - in: formData
        name: isoCode
        description: ISO Code
      - in: formData
        name: sendTime
        description: Timestamp to send fax at
      - in: formData
        name: to
        description: To Phone Number
      responses:
        200:
          description: OK
      tags:
      - Fax
      - Message
  /restapi/v1.0/account/{accountId}/extension/{extensionId}/message-store:
    get:
      summary: Get Message List
      description: "Returns the list of messages from an extension mailbox.\nApp Permission\nReadMessages\nUser
        Permission\nReadMessages\nUsage Plan Group\nLight\nError Codes\n\n \n  \n
        \  HTTP Code\n   Error Code\n   Error Message\n   \n \n\n400\nCMN-101\nParameter
        [readStatus] value is invalid\n\n\n401\nCMN-405\nLogin to extension required\n\n\n401\nOAU-151\nAuthorization
        method not supported\n\n\n403\nCMN-401\nIn order to call this API endpoint,
        application needs to have [ReadMessages] permission\n\n\n403\nCMN-408\nIn
        order to call this API endpoint, user needs to have [ReadMessages] permission
        for requested resource.\n\n\n404\nCMN-102\nResource for parameter [extensionId]
        is not found"
      operationId: listMessages
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidmessagestore-get
      parameters:
      - in: path
        name: accountId
        description: Internal identifier of a RingCentral account or tilde (~) to
          indicate the account logged-in within the current session
      - in: query
        name: availability
        description: Specifies the availability status for the resulting messages
      - in: query
        name: conversationId
        description: Specifies the conversation identifier for the resulting messages
      - in: query
        name: dateFrom
        description: The start datetime for resulting messages in ISO 8601 format
          including timezone, for example 2016-03-10T18:07:52
      - in: query
        name: dateTo
        description: The end datetime for resulting messages in ISO 8601 format including
          timezone, for example 2016-03-10T18:07:52
      - in: query
        name: direction
        description: The direction for the resulting messages
      - in: query
        name: distinctConversations
        description: If True, then the latest messages per every conversation ID are
          returned
      - in: path
        name: extensionId
        description: Internal identifier of an extension or tilde (~) to indicate
          the extension assigned to the account logged-in within the current session
      - in: query
        name: messageType
        description: The type of the resulting messages
      - in: query
        name: page
        description: Indicates the page number to retrieve
      - in: query
        name: perPage
        description: Indicates the page size (number of items)
      - in: query
        name: phoneNumber
        description: The phone number
      - in: query
        name: readStatus
        description: The read status for the resulting messages
      responses:
        200:
          description: OK
      tags:
      - Message
      - List
  /restapi/v1.0/account/{accountId}/extension/{extensionId}/message-store/{messageId}/content/{attachmentId}:
    get:
      summary: Get Message Attachment
      description: "Returns a specific message attachment data as a media stream.\nApp
        Permission\nReadMessages\nUser Permission\nReadMessageContent\nUsage Plan
        Group\nMedium\nError Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error
        Message\n   \n \n\n401\nAGW-402\nInvalid Authorization header\n\n\n401\nCMN-405\nLogin
        to extension required\n\n\n401\nOAU-149\nUnparsable access token\n\n\n401\nOAU-151\nAuthorization
        method not supported\n\n\n403\nCMN-401\nIn order to call this API endpoint,
        application needs to have [ReadMessages] permission\n\n\n403\nCMN-408\nIn
        order to call this API endpoint, user needs to have [ReadMessageContent] permission
        for requested resource.\n\n\n404\nCMN-102\nResource for parameter [extensionId]
        is not found\n\n\n416\nCMN-107\nRequested range not satisfiable"
      operationId: preturns-a-specific-message-attachment-data-as-a-media-streamph4app-permissionh4preadmessagesph4user
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidmessagestoremessageidcontentattachmentid-get
      parameters:
      - in: path
        name: accountId
        description: Internal identifier of a RingCentral account or tilde (~) to
          indicate the account logged-in within the current session
      - in: path
        name: attachmentId
        description: Internal identifier of a message attachment
      - in: path
        name: extensionId
        description: Internal identifier of an extension or tilde (~) to indicate
          the extension assigned to the account logged-in within the current session
      - in: path
        name: messageId
        description: Internal identifier of a message
      - in: header
        name: Range
      responses:
        200:
          description: OK
      tags:
      - Message
      - Attachment
  /restapi/v1.0/account/{accountId}/extension/{extensionId}/message-sync:
    get:
      summary: Get Message Sync
      description: "Synchronizes messages.\nApp Permission\nReadMessages\nUser Permission\nReadMessages\nUsage
        Plan Group\nLight\nError Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error
        Message\n   \n \n\n400\nCMN-101\nParameter [messageType] value is invalid\n\n\n400\nMSG-333\nParameter
        [syncToken] is invalid\n\n\n403\nCMN-401\nIn order to call this API endpoint,
        application needs to have [ReadMessages] permission\n\n\n403\nCMN-408\nIn
        order to call this API endpoint, user needs to have [ReadMessages] permission
        for requested resource.\n\n\n404\nCMN-102\nResource for parameter [extensionId]
        is not found"
      operationId: syncMessages
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidmessagesync-get
      parameters:
      - in: path
        name: accountId
        description: Internal identifier of a RingCentral account or tilde (~) to
          indicate the account logged-in within the current session
      - in: query
        name: conversationId
        description: Conversation identifier for the resulting messages
      - in: query
        name: dateFrom
        description: The start datetime for resulting messages in ISO 8601 format
          including timezone, for example 2016-03-10T18:07:52
      - in: query
        name: dateTo
        description: The end datetime for resulting messages in ISO 8601 format including
          timezone, for example 2016-03-10T18:07:52
      - in: query
        name: direction
        description: Direction for the resulting messages
      - in: query
        name: distinctConversations
        description: If True, then the latest messages per every conversation ID are
          returned
      - in: path
        name: extensionId
        description: Internal identifier of an extension or tilde (~) to indicate
          the extension assigned to the account logged-in within the current session
      - in: query
        name: messageType
        description: Type for the resulting messages
      - in: query
        name: recordCount
        description: Limits the number of records to be returned (works in combination
          with dateFrom and dateTo if specified)
      - in: query
        name: syncToken
        description: Value of syncToken property of last sync request response
      - in: query
        name: syncType
        description: Type of message synchronization
      responses:
        200:
          description: OK
      tags:
      - Message
      - Sync
  /restapi/v1.0/account/{accountId}/extension/{extensionId}/message-store/{messageId}:
    get:
      summary: Get Message(s) by ID
      description: "Returns individual message record(s) by the given message ID(s).
        The length of inbound messages is unlimited. Batch request is supported.\nApp
        Permission\nReadMessages\nUser Permission\nReadMessages\nUsage Plan Group\nLight\nError
        Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error Message\n   \n \n\n401\nCMN-405\nLogin
        to extension required\n\n\n401\nOAU-151\nAuthorization method not supported\n\n\n403\nCMN-401\nIn
        order to call this API endpoint, application needs to have [ReadMessages]
        permission\n\n\n403\nCMN-408\nIn order to call this API endpoint, user needs
        to have [ReadMessages] permission for requested resource.\n\n\n404\nCMN-102\nResource
        for parameter [extensionId] is not found"
      operationId: loadMessage
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidmessagestoremessageid-get
      parameters:
      - in: path
        name: accountId
        description: Internal identifier of a RingCentral account or tilde (~) to
          indicate the account logged-in within the current session
      - in: path
        name: extensionId
        description: Internal identifier of an extension or tilde (~) to indicate
          the extension assigned to the account logged-in within the current session
      - in: path
        name: messageId
        description: Internal identifier of a message
      responses:
        200:
          description: OK
      tags:
      - Message(s)
      - By
      - ID
    put:
      summary: Update Message(s) by ID
      description: "Updates message(s) by ID(s). Batch request is supported, see Batch
        Requests for details. Currently, only the message read status updating is
        supported.\nApp Permission\nEditMessages\nUser Permission\nEditMessages\nUsage
        Plan Group\nMedium\nError Codes\n\n \n  \n   HTTP Code\n   Error Code\n   Error
        Message\n   \n \n\n400\nCMN-101\nParameter [] value is invalid\n\n\n403\nCMN-401\nIn
        order to call this API endpoint, application needs to have [EditMessages]
        permission\n\n\n403\nCMN-408\nIn order to call this API endpoint, user needs
        to have [EditMessages] permission for requested resource.\n\n\n404\nCMN-102\nResource
        for parameter [extensionId] is not found"
      operationId: updateMessage
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidmessagestoremessageid-put
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
      - in: path
        name: messageId
        description: Internal identifier of a message
      responses:
        200:
          description: OK
      tags:
      - Message(s)
      - By
      - ID
    delete:
      summary: Delete Message(s) by ID
      description: "Deletes message(s) by the given message ID(s). The first call
        of this method transfers the message to the &#39;Delete&#39; status. The second
        call transfers the deleted message to the &#39;Purged&#39; status. If it is
        required to make the message &#39;Purged&#39; immediately (from the first
        call), then set the query parameter purge to &#39;True&#39;.\nApp Permission\nEditMessages\nUser
        Permission\nEditMessages\nUsage Plan Group\nMedium\nError Codes\n\n \n  \n
        \  HTTP Code\n   Error Code\n   Error Message\n   \n \n\n400\nCMN-101\nParameter
        [purge] value is invalid\n\n\n403\nCMN-401\nIn order to call this API endpoint,
        application needs to have [EditMessages] permission\n\n\n403\nCMN-408\nIn
        order to call this API endpoint, user needs to have [EditMessages] permission
        for requested resource.\n\n\n404\nCMN-102\nResource for parameter [extensionId]
        is not found"
      operationId: deleteMessage
      x-api-path-slug: restapiv1-0accountaccountidextensionextensionidmessagestoremessageid-delete
      parameters:
      - in: path
        name: accountId
        description: Internal identifier of a RingCentral account or tilde (~) to
          indicate the account logged-in within the current session
      - in: query
        name: conversationId
        description: Internal identifier of a message thread
      - in: path
        name: extensionId
        description: Internal identifier of an extension or tilde (~) to indicate
          the extension assigned to the account logged-in within the current session
      - in: path
        name: messageId
        description: Internal identifier of a message
      - in: query
        name: purge
        description: If the value is True, then the message is purged immediately
          with all the attachments
      responses:
        200:
          description: OK
      tags:
      - Message(s)
      - By
      - ID
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