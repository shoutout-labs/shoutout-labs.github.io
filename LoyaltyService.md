## Loyalty Service

Loyalty service available as an API. This service allows a merchant to easily integrate a loyalty system to a business which serves customers.

### <a id="#rH"></a>How it Works

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

### <a id="#rA"></a>RESTful API

We have a very simple RESTful API with mainly three endpoints. And both endpoints receives request data as JSON objects.

 1. Register Users
 2. Collect Points
 3. Redeem Points

#### <a id="#2"></a>Register Users

This is a merchant specific endpoint and would be created upon request based on the merchant specific parameters

#### <a id="#2"></a>Collect Points

**Sample curl command**

```curl
curl -X POST \
  https://getshoutout.com/v8/points \
  -H 'authorization: Bearer <API_KEY>' \
  -H 'content-type: application/json' \
  -d '{
  "userId":"LOYAL-USER-001",
  "activityData":{
	  "bill":2350.00,
	  "bill_number":"INV-001",
	  "employee":"Smith",
	}
}'
```

#### <a id="#3"></a>Redeem Points

**Sample curl command**

```curl
curl -X POST \
  https://getshoutout.com/v8/points \
  -H 'authorization: Bearer <API_KEY>' \
  -H 'content-type: application/json' \
  -d '{
  "userId":"LOYAL-USER-001",
  "activityData":{
	 "points":-17,
	 "employee":"Smith",
	 "location":"Colombo"
	 }
 }'
```

### Questions or Problems ?

If you run into any difficulties or can't get something to work. Don't hesitate to contact us via <support@getshoutout.com>. We would love to help you out.

<small>Copyright © 2017. ShoutOUT Labs. All Rights Reserved.</small>