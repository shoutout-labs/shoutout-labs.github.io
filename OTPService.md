## One Time Password Service

### <a id="#rH"></a>How it Works

<div style="text-align:center"><img src ="http://developers.getshoutout.com/images/OTP_Service_Message_Flow.png" /></div>


1. User provide mobile number to your application
2. Your application make send OTP request to OTP service with mobile number and store the reference id
3. OTP service send a SMS with a code to the mobile number in step 2
4. User provide the received code to your application
5. Your application make make verify OTP request to OTP service with code and reference id received in step 2 and receive the verify status

### <a id="#rA"></a>RESTful API

We have a very simple RESTful API with mainly two endpoints. And both endpoints receives request data as JSON objects.

 1. Send OTP
 2. Verify OTP

#### <a id="#1"></a>Send OTP

**Sample curl command**

```curl
curl -X POST
--header 'Content-Type: application/json'
--header 'Accept: application/json'
--header 'Authorization: Apikey <API_KEY>'
-d '{
  "destination": "94777123456",
  "source": "ShoutDEMO",
  "transport": "sms",
  "content": {
    "sms": "Hi Duke! Your code is {{code}}"
  }
}' 'https://getshoutout.com/v1/otp/send'
```

#### <a id="#2"></a>Verify OTP

**Sample curl command**

```curl
curl -X POST
--header 'Content-Type: application/json'
--header 'Accept: application/json'
--header 'Authorization: Apikey <API_KEY>'
-d '{
  "code": "ABCDE",
  "referenceId": "f437c171-2d08-48c8-a4a2-92a6aff7e853"
}' 'https://getshoutout.com/v1/otp/verify'
```

### Questions or Problems ?

If you run into any difficulties or can't get something to work. Don't hesitate to contact us via <support@getshoutout.com>. We would love to help you out.

<small>Copyright © 2017. ShoutOUT Labs. All Rights Reserved.</small>