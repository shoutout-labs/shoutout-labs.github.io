---
title: /otp/verify
position: 1.3
type: post
description: Send One Time Password
parameters:
  - name: code
    content: One time password
  - name: referenceId
    content: Refence id received in send otp response
content_markdown: |-

  If valid successful response will be received
left_code_blocks:
  - code_block: |-
      curl -X POST
      --header 'Content-Type: application/json'
      --header 'Accept: application/json'
      --header 'Authorization: Apikey <API_KEY>'
      -d '{
        "code": "ABCDE",
        "referenceId": "f437c171-2d08-48c8-a4a2-92a6aff7e853"
      }' 'https://getshoutout.com/v1/otp/verify'
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


