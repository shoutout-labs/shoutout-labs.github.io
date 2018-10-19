---
title: /users/:id
position: 1.3
type: get
description: Load user profile
parameters:
  - name:
    content:
content_markdown: |-
  <b>:id</b> is the value of user's loyalty id
  {: .info}

  Returns the profile of the user
left_code_blocks:
  - code_block: |-
      $.get("https://api.getshoutout.com/loyaltyservice/users/:id", {
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |2-
      {
        "name": "John",
        "loyalty_id": "LOYAL-USER-001",
        "points": 17,
        "tier": "Level 1",
        "tier_points": 15,
        "benefits": [
          "10% Discount on all products"
        ]
      }
    title: Response
    language: json
  - code_block: |2-
      {
        "message": "<error message>"
      }
    title: Error
    language: json
---