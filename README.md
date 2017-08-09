### Integrate with ShoutOUT

Integrating with ShoutOUT is very easy. You have two options.

 1. Use our client library to connect to our RESTful API
 2. Directly connect to our RESTful API

### <a id="#cL"></a>SDKs & Client Libraries

We maintain client libraries for several languages to connect to our RESTful API.

- [NodeJS](https://www.npmjs.com/package/shoutout-sdk)
- [PHP](https://packagist.org/packages/shoutoutlabs/shoutout-sdk)
- [Java](https://github.com/shoutout-labs/shoutout-sdk-java)

### <a id="#rA"></a>RESTful API

We have a very simple RESTful API with mainly three endpoints. And all three endpoints receives request data as JSON objects.

 1. Create or update contact(s)
 2. Create activity
 3. Send message


#### <a id="#1"></a>Create or Update Contact(s)

**Sample curl command**

```curl
curl -X POST 
--header 'Content-Type: application/json' 
--header 'Accept: application/json' 
--header 'Authorization: Apikey <API_KEY>' 
-d '[{
        user_id: '94777123456',
        mobile_number: '94777123456',
        email: 'duke@test.com',
        name: 'Duke',
        tags: ['lead']
    }]' 'https://getshoutout.com/api/v8/contacts'
```

#### <a id="#2"></a>Create Activity

**Sample curl command**

```curl
curl -X POST 
--header 'Content-Type: application/json' 
--header 'Accept: application/json' 
--header 'Authorization: Apikey <API_KEY>' 
-d '{
        userId: '94777123456',
        activityName: 'Sample Activity',
        activityData: {
            param1: 'val1',
            param2: 'val2',
            param3: 'val3'
        }
    }' 'https://getshoutout.com/v8/activities'
```

#### <a id="#3"></a>Send Message

**Sample curl command**

```curl
curl -X POST 
--header 'Content-Type: application/json' 
--header 'Accept: application/json' 
--header 'Authorization: Apikey <API_KEY>' 
-d '{
        source: 'ShoutDEMO',
        destinations: ['94777123456'],
        content: {
            sms: 'Sent via SMS Gateway'
        },
        transports: ['sms']
    }' 'https://getshoutout.com/v7/messages'
```

### Questions or Problems ?

If you run into any difficulties or can't get something to work. Don't hesitate to contact us via <support@getshoutout.com>. We would love to help you out.

<small>Copyright © 2017. ShoutOUT Labs. All Rights Reserved.</small>