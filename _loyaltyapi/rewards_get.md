---
title: /rewards
position: 1.9
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


