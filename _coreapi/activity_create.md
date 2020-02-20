---
title: /activities
position: 1.3
type: post
description: Create Activity
parameters:
  - name: userId
    content: Userid which was used to create the contact
  - name: activityName
    content: Name of the activity
  - name: activityData
    content: JSON object with arbitary data
content_markdown: |-
  A new event will be created with the activity name if not already created
  {: .success}

  Create an activity for the user
left_code_blocks:
  - code_block: |-
      $.post("https://api.getshoutout.com/coreservice/activities", {
        "userId":"94777123456",
        "activityName":"Test Event",
        "activityData":{
          "param1":"val1"
        }
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript

  # - code_block: |-
     
  #   title: Curl
  #   language: bash

  - code_block: |-
      
      var activity = {
          userId: '94777123456',
          activityName: 'Sample Activity',
          activityData: {
             param1: 'val1',
             param2: 'val2',
             param3: 'val3'
         }
      };
 
      client.createActivity(activity, (error, result) => {
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


        $activity = array(
            'userId' => '94777123456',//Required. your account id
            //arbitrary attributes
            'activityName' => 'Sample Activity',
            'activityData' => array(
                'param1' => 'val1',
                'param2' => 'val2',
               'param3' => 'val3'
            )
        );

        try {
            $result = $client->createActivity($activity);
            print_r($result);
        } catch (Exception $e) {
            echo 'Exception when creating activity ', $e->getMessage(), PHP_EOL;
        }

        ?>
     
    title: PHP
    language: bash

right_code_blocks:
  - code_block: |-
      {
        "userId": "94777123456",
        "activityName": "Test Event",
        "activityData": {
          "param1": "val1"
        },
        "createdOn": "2019-01-11T07:35:24.054Z",
        "_id": "xxxxxxxxx",
        "eventId": "3a3be55cafb08ed1878fe0ab7dbxxxxxxxx",
        "contactId": "66f019b8c509667d065055e4xxxxxx"
      }
    title: Response
    language: json
  - code_block: |-
      {
        "message": "Authentication Failure!"
      }
    title: Error
    language: json
---


