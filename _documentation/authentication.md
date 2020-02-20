---
title: Authentication
position: 1.5
parameters:
  - name:
    content:
content_markdown: |-
  You need to be authenticated for all API requests. You can generate an API key in our developer dashboard.

  Add the API key to all requests as a header

  Nothing will work unless you include this API key
  {: .error}
left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block: |2-
       Authorization: Apikey <API_KEY>
    title: HTTP Header
    language: bash
---