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
        "id": 3,
        "title": "The Book Thief",
        "score": 4.3,
        "dateAdded": "5/1/2015"
      }
    title: Response
    language: json
  - code_block: |2-
      {
        "error": true,
        "message": "Book doesn't exist"
      }
    title: Error
    language: json
---