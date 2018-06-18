---
title: /logs/{id}
position: 1.3
type: get
description: Get log for message id
parameters:
  - name: id
    content: Message id
content_markdown: |-
  Message id should be mentioned on the path
  {: .warning}

left_code_blocks:
  - code_block: |-
      $.get("https://api.getshoutout.com.com/coreservice/logs/{id}", {
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
  - code_block: |-
      curl -X GET 
      --header 'Content-Type: application/json' 
      --header 'Accept: application/json' 
      --header 'Authorization: Apikey <API_KEY>' 
      'https://api.getshoutout.com/coreservice/logs/{id}'
    title: Curl
    language: bash
right_code_blocks:
  - code_block: |-
      {
        "id": "{id}",
        "status": "1000"
      }

      Message Status
        1000 - Queued
        1001 - Sucess
        1010 - Internal Error
        1012 - No Route
        1015 - Blocked
        1026 - Submitted
    title: Response
    language: json
---


