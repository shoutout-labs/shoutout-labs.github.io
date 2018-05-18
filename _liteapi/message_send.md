---
title: /messages
position: 1.2
type: post
description: Send SMS Message
parameters:
  - name: source
    content: Sender mask (Alias)
  - name: destinations
    content: Mobile numbers in E.164 format
  - name: content
    content: JSON object with key "sms" and the message content in the value
  - name: transports
    content: String array, ["sms"]
content_markdown: |-
  Message will be logged and can be viewed from the dashboard
  {: .info}

  Send sms message(s) to the destination addresse(s)
left_code_blocks:
  - code_block: |-
      $.post("https://api.getshoutout.com.com/coreservice/messages", {
        "source": "ShoutDEMO",
        "destinations": ["+94777123456"],
        "content": {
          "sms":"Sent via SMS Gateway"
        },
        "transports":["sms"]
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
  - code_block: |-
      curl -X POST 
      --header 'Content-Type: application/json' 
      --header 'Accept: application/json' 
      --header 'Authorization: Apikey <API_KEY>' 
      -d '{
        source: 'ShoutDEMO',
        destinations: ['94777123456'],
        content: {
            sms: 'Sent via SMS Gateway'
        },
        transports: ['sms']
      }' 'https://api.getshoutout.com/coreservice/messages'
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


