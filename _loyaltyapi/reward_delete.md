---
title: /rewards/:id
position: 1.8
type: delete
description: Delete reward
parameters:
  - name: 
    content: 
content_markdown: |-

  Reward with the id mentioned on the url will be deleted
left_code_blocks:
  - code_block: |-
      curl -X POST \
        https://api.getshoutout.com/loyaltyservice/points \
        -H 'authorization: Bearer <API_KEY>' \
        -H 'content-type: application/json' \
        -d '{
        "userId":"LOYAL-USER-001",
        "activityData":{
        "points":-17,
        "employee":"Smith",
        "location":"Colombo"
        }
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


