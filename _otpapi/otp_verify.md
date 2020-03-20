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
        "referenceId": "f437c171-2d08-48c8-a4a2-xxxxxxxx"
      }' 'https://api.getshoutout.com/otpservice/verify'
    title: Curl
    language: bash

  - code_block: |-
       $.post("https://api.getshoutout.com/otpservice/verify", [{
        "code": "ABCDE",
        "referenceId": "f437c171-2d08-48c8-a4a2-xxxxxxxx",
       }], function(data) {
        alert(data);
       });
    title: JQuery
    language: javascript

  # - code_block: |-
     
  #   title: Node
  #   language: javascript

  # - code_block: |-
     
  #   title: PHP
  #   language: bash

right_code_blocks:
  - code_block: |-
     {
       "referenceId": "f437c171-2d08-48c8-a4a2-xxxxxxxx",
       "code": "87XXX",
       "statusCode": "1000",
       "description": "verification success"
     }
    title: Response
    language: json
  - code_block: |-
     {
        "message": "<error message>"
     }
    title: Error
    language: json
---


