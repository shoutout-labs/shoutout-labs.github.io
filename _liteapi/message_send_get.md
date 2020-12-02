---
title: /messages
position: 1.5
type: get
description: Send SMS Message (Use this method only if the POST method can't be used)
parameters:
  - name: source
    content: String (Sender mask/alias)
  - name: destinations
    content: Array<String> (Array of mobile numbers in E.164 format)
  - name: content
    content: String (SMS message content)
  - name: apiKeyId
    content: String (ID of the API Key)
content_markdown: |-
  Message will be logged and can be viewed from the dashboard
  {: .info}

  Send sms message(s) to the destination addresse(s)
left_code_blocks:

  - code_block: |-
      curl --request GET 'https://api.getshoutout.com/coreservice/messages?source=ShoutDEMO&destinations[]=94777123456&content=Test%20SMS&apiKeyId=xxxxxxx-xxxx-xxx-xxx-xxxxx'
    title: Curl
    language: bash

  - code_block: |-
      var settings = {
        "url": "https://api.getshoutout.com/coreservice/messages?source=ShoutDEMO&destinations[]=94777123456&content=Test SMS&apiKeyId=xxxxxxx-xxxx-xxx-xxx-xxxxx",
        "method": "GET"
      };
      
      $.ajax(settings).done(function (response) {
        console.log(response);
      });
    title: jQuery
    language: javascript


right_code_blocks:
  - code_block: |-
      {
        "destination": "94777123456",
        "reference_id": "c6193930-5165-11ea-9bc0-d9d9952d720b",
        "status": "1001",
        "cost": 1
      }
    title: Response
    language: json

  - code_block: |-
      {
          "status": "1007",
          "description": "invalid source"
      }
    title: Source Error
    language: json

    right_code_blocks:
  - code_block: |-
       {
         "status": "1005",
         "description": "invalid request, \"value\" at position X fails because [\"X\" needs to be a valid phone number according to E.164 international format]"
       }
    title: Destinaion Error
    language: json


---


