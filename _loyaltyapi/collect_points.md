---
title: /points Collect
position: 1.4
type: post
description: Add points to user
parameters:
  - name: userId
    content: Loyalty id of the user
  - name: activityData
    content: JSON object with required key "bill" or "points" and any other arbitary keys
content_markdown: |-
  Make sure you include either <b>bill</b> or <b>points</b> in the <b>activityData</b> object
  {: .warning}

  Points will be calculated by the system and added to the user accordingly
left_code_blocks:

  - code_block: |-
      curl -X POST \
        https://api.getshoutout.com/loyaltyservice/points?action=collect \
        -H 'authorization: Bearer <API_KEY>' \
        -H 'content-type: application/json' \
        -d '{
        "userId":"LOYAL-USER-001",
        "activityData":{
          "bill":2350.00,
          "bill_number":"INV-001",
          "employee":"Smith",
          "location":"Main Branch"
        }
      }'
    title: Curl
    language: bash

  - code_block: |-
       $.post("https://api.getshoutout.com/loyaltyservice/points?action=collect", [{
        "user_id": "LOYAL-USER-001",
        "activityData":{
          "bill":2350.00,
          "bill_number":"INV-001",
          "employee":"Smith",
          "location":"Main Branch"
        }
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
        "points": 100,
         "tier_points": 1,
        "total_points": 200,
        "loyalty_id": "SPO-1"
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


