---
title: Authentication
position: 2
parameters:
  - name:
    content:
content_markdown: |-
  You need to be authenticated for all API requests. You can generate an API key in our developer dashboard.

  Add the API key to all requests as a header in the following format

  Header name : Authorization
  Header value : Apikey <YOUR_API_KEY>

  Nothing will work unless you include this API key
  {: .error}
left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block: |2-
       curl  -H "Authorization: Apikey <YOUR_API_KEY>" -X POST http://api.getshoutout.com/coreservice/messages
    title: Curl
    language: bash
---