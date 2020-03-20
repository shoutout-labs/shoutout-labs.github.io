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
     {
       curl --location --request POST ‘https://api.getshoutout.com/otpservice/send’ \
       --header ‘Content-Type: application/json’ \
       --header ‘Authorization: Apikey XXX.XXX.XXXX’ \
       --data-raw ‘{
        “source”:“ShoutDEMO”,
        “transport”:“sms”,
        “content”:{
          “sms”:“Your code is {{code}}”
        },
        “destination”:“9477xxxxxxx”
      }’
     }

    title: Curl
    language: bash
       
  - code_block: |-
        $.post("https://api.getshoutout.com/otpservice/send", [{
        "source": "ShoutDEMO",
        "transport": "sms",
        "content": {
          "sms":"Your code is {{code}}"
        },
        "destination":"9477xxxxxxx"
        }], function(data) {
        alert(data);
        });
    title: JQuery
    language: javascript

  # - code_block: |-
  #     {
        
  #     }
  #   title: Node
  #   language: javascript

  # - code_block: |-
  #     {
        
  #     }
  #   title: PHP
  #   language: bash

  

right_code_blocks:
  - code_block: |-
      {
       "referenceId": "f437c171-2d08-48c8-a4a2-xxxxxxxx",
       "messageResult": {
         "status": "1001",
         "description": "submit success",
         "cost": 1,
         "responses": [{
           "destination": "94711234567",
           "reference_id": "82ec4200-d386-11e8-b097-xxxxxxxxxxx",
           "status": "1001",
           "cost": 1
         }]
       } 
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


