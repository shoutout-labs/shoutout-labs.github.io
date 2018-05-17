---
title: Introduction
position: 1.1
parameters:
  - name:
    content:
content_markdown: |-
  Loyalty service available as an API. This service allows a merchant to easily integrate a loyalty system to a business which serves customers

  <div style="text-align:center"><img src ="http://developers.getshoutout.com/images/Loyalty_Service_Overview.png" /></div>
  
  #### User Registration

  1. Merchant submit the customer details to loyalty service using one of the following
  - Hosted registration form
  - Embedded registration form
  - Direct API call
  2. Optionally customer receives a SMS or an Email with a welcome message and details of his/her loyalty account

  #### Point Collection

  1. Merchant record customer transactions in the PoS system
  2. PoS system sends the bill value along with other transaction details to the collect points API endpoint of ShoutOUT Loyalty service
  3. ShoutOUT Loyalty service calculate the points for the bill value and accumulate it to the customer points pool
  4. Optionally a SMS or an Email is sent to the customer with the details of the transaction and points accumulation.

  ### RESTful API

  We have a very simple RESTful API with mainly four endpoints. And all endpoints receives request data as JSON objects.

  1. Register User
  2. Load User
  3. Collect Points
  4. Redeem Points
left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block:
    title:
    language:
---