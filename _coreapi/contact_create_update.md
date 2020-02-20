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
        curl -X POST 
        --header 'Content-Type: application/json' 
        --header 'Accept: application/json' 
        --header 'Authorization: Apikey <API_KEY>' 
        -d '{
         "user_id": "94777123456",
        "name": "Duke",
        "mobile_number": "94777123456",
        "email": "duke@test.com"
        }' 'https://api.getshoutout.com/coreservice/contacts'
    title: Curl
    language: bash
    
  - code_block: |-
      $.post("https://api.getshoutout.com/coreservice/contacts", [{
        "user_id": "94777123456",
        "name": "Duke",
        "mobile_number": "94777123456",
        "email": "duke@test.com"
      }], function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript


  - code_block: |-
    
        var contacts = [{
             user_id: '94777123456',
              mobile_number: '94777123456',
              email: 'duke@test.com',
              name: 'Duke',
              tags: ['lead']
              }];
 
        client.createContacts(contacts, (error, result) => {
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


        $contact = array(
            'mobile_number' => '94777123456',//Required if not specified user_id
            'user_id' => '94777123456',//Optional. if specified, this will be used to generate the contact id, otherwise         mobile_number will be used to generate contact id
            //arbitrary attributes
            'email' => 'duke@test.com',
            'tags' => ['lead'],
            'name' => 'Duke'
        );
            $contacts = array($contact);

        try {
            $result = $client->createContacts($contacts);
            print_r($result);
        } catch (Exception $e) {
            echo 'Exception when creating contacts ', $e->getMessage(), PHP_EOL;
        }

        ?>
      
      
    title: PHP
    language: bash


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


