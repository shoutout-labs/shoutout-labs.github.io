---
title: /rewards
position: 1.2
type: post
description: Create Reward
parameters:
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
        https://api.getshoutout.com/loyaltyservice/rewards/
        -H 'authorization: Bearer <API_KEY>' \
        -H 'content-type: application/json' \
        -d '{
        "name": "rewards",
        "description" : "",
        "type": "voucher",
        "userRedeemable": "false",
        "points": 1,
        "status" : 2,
        "imageUrls": [
        "https://gallery.getshoutout.com/sample.jpeg"
        ],
        "metadata": { 
          "dailyRedemptionLimit":2,
          "amountPerRedemption":2,
          "amountPerRedemptionSeasonal": {
            "value": 2,
            "searchFromDate": "2019-09-09",
            "searchToDate": "2020-02-02"
            },
           "digitalRewardInfo" :{
        	    "type":""
             }
          }
        }'
    title: Curl
    language: bash

  - code_block: |-
      $.post(" https://api.getshoutout.com/loyaltyservice/rewards/ ", {
        "name": "rewards",
        "description" : "",
        "type": "voucher",
        "userRedeemable": "false",
        "points": 1,
        "status" : 2,
        "imageUrls": [
        "https://gallery.getshoutout.com/sample.jpeg"
        ],
        "metadata": { 
          "dailyRedemptionLimit":2,
          "amountPerRedemption":2,
          "amountPerRedemptionSeasonal": {
            "value": 2,
            "searchFromDate": "2019-09-09",
            "searchToDate": "2020-02-02"
            },
           "digitalRewardInfo" :{
        	    "type":""
             }
          }
        }', function(data) {
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
        "rewardName": "Sample Reward",
        "points": 10,
        "imageUrls": ["https://gallery.getshoutout.com/sample.jpeg"],
        "rewardStatus": 0,
        "rewardId": "bc0c9680-59be-11e8-82ea-7154ab678cae",
        "createdOn": "2018-05-01T10:40:36.841Z",
        "updatedOn": "2018-05-01T10:40:36.841Z"
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


