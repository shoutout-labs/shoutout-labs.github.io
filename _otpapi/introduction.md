---
title: Introduction
position: 1.1
parameters:
  - name:
    content:
content_markdown: |-
  Easy mobile number verification service available as an API. This service allows an application to easily send a system generated code to a mobile number and verify it programmatically. This can be used for two factor authentication, mobile number verification and one time password (magic passwords) like use cases.

  #### How it Works

  <div style="text-align:center"><img src ="http://developers.getshoutout.com/images/OTP_Service_Message_Flow.png" /></div>
  
  1. User provide mobile number to your application
  2. Your application make send OTP request to OTP service with mobile number and store the reference id received
  3. OTP service send a SMS with a code to the mobile number
  4. User provide the received code to your application
  5. Your application make verify OTP request to OTP service with code and reference id and receive the verify status
left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block:
    title:
    language:
---