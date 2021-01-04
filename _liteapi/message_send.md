---
title: /messages
position: 1.4
type: post
description: Send SMS Message (Recommended method)
parameters:
  - name: source
    content: Sender mask (Alias)
  - name: destinations
    content: Mobile numbers in E.164 format
  - name: content
    content: JSON object with key "sms" and the message content in the value
  - name: transports
    content: String array, ["sms"]
content_markdown: |-
  Message will be logged and can be viewed from the dashboard
  {: .info}

  Send sms message(s) to the destination addresse(s)
left_code_blocks:

  - code_block: |-
        curl --location --request POST 'https://api.getshoutout.com/coreservice/messages' \
        --header 'Authorization: Bearer <API_KEY>' \
        --header 'Content-Type: application/json' \
        --data-raw '{
          "source": "ShoutDEMO",
          "destinations": ["94777123456"],
          "content": {
              "sms": "Sent via SMS Gateway"
          },
          "transports": ["sms"]
        }'
    title: Curl
    language: bash

  - code_block: |-
      $.post("https://api.getshoutout.com/coreservice/messages", {
        "source": "ShoutDEMO",
        "destinations": ["+94777123456"],
        "content": {
          "sms":"Sent via SMS Gateway"
        },
        "transports":["sms"]
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript

  

  - code_block: |-
        var message = {
          source: 'ShoutDEMO',
          destinations: ['94777123456'],
           content: {
               sms: 'Sent via SMS Gateway'
          },
           transports: ['sms']
        };
        client.sendMessage(message, (error, result) => {
          if (error) {
              console.error('error ', error);
          } else {
              console.log('result ', result);
          }
        });
    title: Node
    language: javascript


  - code_block: |-
     
       <?php

       require __DIR__ . '/vendor/autoload.php';

       use Swagger\Client\ShoutoutClient;

       $apiKey = 'XXXXXXXXX.XXXXXXXXX.XXXXXXXXX';

       $client = new ShoutoutClient($apiKey,true,false);


       $message = array(
           'source' => 'ShoutDEMO',
           'destinations' => ['94777123456'],
           'content' => array(
               'sms' => 'Sent via SMS Gateway'
           ),
           'transports' => ['SMS']
       );

       try {
           $result = $client->sendMessage($message);
           print_r($result);
       } catch (Exception $e) {
           echo 'Exception when sending message: ',  $e->getMessage(), PHP_EOL;
       }

       ?>
     

    title: PHP
    language: bash



right_code_blocks:
  - code_block: |-
      {
        "destination": "94777123456",
        "reference_id": "c6193930-5165-11ea-9bc0-d9d9952d720b",
        "status": "1001",
        "cost": 1
      }
    title: Response
    language: json

  - code_block: |-
      {
          "status": "1007",
          "description": "invalid source"
      }
    title: Source Error
    language: json

    right_code_blocks:
  - code_block: |-
       {
         "status": "1005",
         "description": "invalid request, \"value\" at position X fails because [\"X\" needs to be a valid phone number according to E.164 international format]"
       }
    title: Destinaion Error
    language: json


---


