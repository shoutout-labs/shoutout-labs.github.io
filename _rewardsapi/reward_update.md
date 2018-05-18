---
title: /rewards
position: 1.7
type: put
description: Update Reward
parameters:
  - name: rewardId
    content: Reward id
  - name: rewardName
    content: Name of the reward
  - name: points
    content: Number of points required to redeem the reward
  - name: rewardStatus
    content: Status of the reward (0-Unpublished,1-Published)
  - name: imageUrls
    content: Array of image urls
content_markdown: |-

  Points will be redeemed from the user's loyalty account
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
        "rewardStatus": 1,
        "updatedOn": "2018-05-17T10:47:02.982Z",
        "rewardName": "Sample Reward",
        "createdOn": "2018-05-01T10:40:36.841Z",
        "points": 10,
        "rewardId": "bc0c9680-59be-11e8-82ea-7154ab678cae",
        "imageUrls": ["https://gallery.getshoutout.com/sample.jpeg"]
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


