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
      curl -X DELETE \
        https://api.getshoutout.com/loyaltyservice/rewards/bc0c9680-59be-11e8-82ea-7154ab678cae \
        -H 'authorization: Bearer <API_KEY>' \
        -H 'content-type: application/json'
      }'
    title: Curl
    language: bash
right_code_blocks:
  - code_block: |-
      {}
    title: Response
    language: json
  - code_block: |-
      {
        "message": "Something went wrong"
      }
    title: Error
    language: json
---


