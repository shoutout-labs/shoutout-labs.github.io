---
title: /rewards
position: 1.5
type: get
description: Get rewards
parameters:
  - name: 
    content: 
content_markdown: |-

  Points will be redeemed from the user's loyalty account
left_code_blocks:
 
  - code_block: |-
      curl -X GET \
        https://api.getshoutout.com/loyaltyservice/rewards \
        -H 'authorization: Bearer <API_KEY>' \
        -H 'content-type: application/json'
      }'
    title: Curl
    language: bash

  - code_block: |-
       $.get("https://api.getshoutout.com/loyaltyservice/rewards ", [{
        
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
        "Items": [{
          "rewardStatus": 1,
          "updatedOn": "2018-05-17T10:47:02.982Z",
          "rewardName": "Sample Reward",
          "createdOn": "2018-05-01T10:40:36.841Z",
          "points": 10,
          "rewardId": "bc0c9680-59be-11e8-82ea-7154ab678cae",
          "imageUrls": ["https://gallery.getshoutout.com/sample.jpeg"]
        }],
        "Count": 1
      }
    title: Response
    language: json
  - code_block: |-
      {
        "message": "Something went wrong"
      }
    title: Error
    language: json
---


