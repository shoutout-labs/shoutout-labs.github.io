---
title: /otp/send
position: 1.2
type: post
description: Send One Time Password
parameters:
  - name: source
    content: Sender mask (Alias)
  - name: destination
    content: Mobile number in E.164 format
  - name: content
    content: JSON object with key "sms" and the message content in the value
  - name: transport
    content: sms
content_markdown: |-
  Make sure you include {{code}} in your message content
  {: .warning}

  System generated one time passcode will be sent to the mobile number
left_code_blocks:
  - code_block: |-
      curl -X POST
      --header 'Content-Type: application/json'
      --header 'Accept: application/json'
      --header 'Authorization: Apikey <API_KEY>'
      -d '{
        "destination": "94777123456",
        "source": "ShoutDEMO",
        "transport": "sms",
        "content": {
          "sms": "Hi Duke! Your code is {{ "{{code" }}}}"
        }
      }' 'https://getshoutout.com/v1/otp/send'
    title: Curl
    language: bash
right_code_blocks:
  - code_block: |-
      {
        "id": 3,
        "title": "The Book Thief",
        "score": 4.3,
        "dateAdded": "5/1/2015"
      }
    title: Response
    language: json
  - code_block: |-
      {
        "error": true,
        "message": "Invalid score"
      }
    title: Error
    language: json
---


