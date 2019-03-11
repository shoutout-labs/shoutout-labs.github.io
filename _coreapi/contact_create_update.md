---
title: /contacts
position: 1.2
type: post
description: Create or update contact(s)
parameters:
  - name: user_id
    content: Unique attribute to identify a person in your people list (Ex:- Mobile Number, Email or System Generated User ID)
  - name: name
    content: Name of the person
  - name: mobile_number
    content: Mobile number of the person in E.164 format
  - name: email
    content: Email of the person
  - name: tags
    content: String array of tags (Ex:- ["lead","employee"])
content_markdown: |-
  Additionally to above default parameters, you can define your own custom parameters
  {: .info}

  Create or update contact(s)
left_code_blocks:
  - code_block: |-
      $.post("https://api.getshoutout.com.com/coreservice/contacts", [{
        "user_id": "94777123456",
        "name": "Duke",
        "mobile_number": "94777123456",
        "email": "duke@test.com"
      }], function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
right_code_blocks:
  - code_block: |-
      [
        {
          "user_id": "94777123456",
          "name": "Duke",
          "mobile_number": "94777123456",
          "email": "duke@test.com",
          "country_code": "LK",
          "country": "Sri Lanka",
          "_mobile_number_valid": true,
          "_email_valid": true,
          "id": "xxxxxxxxxxxxxxxxxxxx"
        }
      ]
    title: Response
    language: json
  - code_block: |-
      {
        "message": "Authentication Failure!"
      }
    title: Error
    language: json
---


