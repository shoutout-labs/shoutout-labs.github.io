---
title: /logs/{id}
position: 1.6
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
      curl -X GET 
      --header 'Content-Type: application/json' 
      --header 'Accept: application/json' 
      --header 'Authorization: Apikey <API_KEY>' 
      'https://api.getshoutout.com/coreservice/logs/{id}'
    title: Curl
    language: bash

  - code_block: |-
      $.get("https://api.getshoutout.com/coreservice/logs/{id}", {
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
  

  # - code_block: |-
      
  #   title: Node
  #   language: bash

  # - code_block: |-
      
  #   title: PHP
  #   language: bash
 

right_code_blocks:
  - code_block: |-
      {
        "id": "{id}",
        "from": "ShoutDEMO",
        "to": "94777123456",
        "status": "1000",
        "isDelivered": true,
        "createdOn": "2018-05-01T10:40:36.841Z",
        "modifiedOn": "2018-05-01T10:40:36.841Z"
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


