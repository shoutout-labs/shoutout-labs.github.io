---
title: /messages
position: 1.1
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
  {: .success}

  Send sms message(s) to the destination addresses
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


