# Register pledge endpoint


## `POST /registration/pledges`


## Resource Information
|Property|Value|
|-----|------|
| Response Format | JSON |
| Requires Authentication? | Yes | 

## Parameters

### Path Parameters

| Name | Required | Description|
| ------ | ------ | ------ |
| None|

### Payload Parameters
| Name | Required | Description|
| ------ | ------ | ------ |
| pledge | required | The information of the donor. See the sample payload below. |
| donations | required | The list of pledges by the donor. See the sample payload below. |
| satisfaction | required | The satisfaction rating given by the caller. |


## Example Request
`http://<base_url>/registration/pledges`


### Sample payload
```
{
	"pledge": {
		"donorName": "Maria Dela Cruz",
		"donorNumber": "09221234566",
		"isVip": true 
	},
	"donations": [
		{
			"donationType": "cash",
			"bank": "BPI",
			"amount": 1000
		},
		{
			"donationType": "others",
			"description": "Moral support and prayer",
			"deliveryBy": "Hulk",
			"deliveryContactNumber": "088912323"
		},
		{
			"donationType": "in_kind",
			"items": [
				{
					"name": "surgical masks",
					"unit": "1pc",
					"quantity": 10	
				}
			],
			"deliveryDate": "2020-04-09T06:00:00.000Z",
			"deliveryBy": "Thor",
			"deliveryContactNumber": "088912345"
		},
		{
			"donationType": "food",
			"items": [
				{
					"name": "water",
					"unit": "20ml",
					"quantity": 2
				}
			],
			"deliveryDate": "2020-04-09T06:00:00.000Z",
			"deliveryBy": "Thor",
			"deliveryContactNumber": "088912345",
			"receivedBy": "Ms. Emelita Lavilla"
		}
	],
	"satisfaction": 4
}
```

## Sample response
```
{
  "data": {
    "donations": [
      {
        "amount": 1000.0,
        "bank": "BPI",
        "createdAt": "Thu, 26 Mar 2020 05:57:41 GMT",
        "createdBy": 1,
        "id": 2,
        "isActive": true,
        "isReceived": false,
        "itemId": 1,
        "pledgeId": 2,
        "updatedAt": "Thu, 26 Mar 2020 05:57:41 GMT"
      },
      {
        "createdAt": "Thu, 26 Mar 2020 05:57:41 GMT",
        "createdBy": 1,
        "deliveryBy": "Hulk",
        "deliveryContactNumber": "088912323",
        "deliveryDate": null,
        "id": 4,
        "isActive": true,
        "isReceived": false,
        "itemId": 2,
        "pledgeId": 2,
        "quantity": 1,
        "receivedBy": null,
        "updatedAt": "Thu, 26 Mar 2020 05:57:41 GMT"
      },
      {
        "createdAt": "Thu, 26 Mar 2020 05:57:41 GMT",
        "createdBy": 1,
        "deliveryBy": "Thor",
        "deliveryContactNumber": "088912345",
        "deliveryDate": "Thu, 09 Apr 2020 06:00:00 GMT",
        "id": 5,
        "isActive": true,
        "isReceived": false,
        "itemId": 3,
        "pledgeId": 2,
        "quantity": 1,
        "receivedBy": null,
        "updatedAt": "Thu, 26 Mar 2020 05:57:41 GMT"
      },
      {
        "createdAt": "Thu, 26 Mar 2020 05:57:41 GMT",
        "createdBy": 1,
        "deliveryBy": "Thor",
        "deliveryContactNumber": "088912345",
        "deliveryDate": "Thu, 09 Apr 2020 06:00:00 GMT",
        "id": 6,
        "isActive": true,
        "isReceived": false,
        "itemId": 4,
        "pledgeId": 2,
        "quantity": 1,
        "receivedBy": "Ms. Emelita Lavilla",
        "updatedAt": "Thu, 26 Mar 2020 05:57:41 GMT"
      }
    ],
    "pledge": {
      "createdAt": "Thu, 26 Mar 2020 05:57:41 GMT",
      "createdBy": 1,
      "donorEmail": null,
      "donorName": "Maria Dela Cruz",
      "donorNumber": "09221234566",
      "donorType": null,
      "id": 2,
      "isActive": true,
      "isReceived": false,
      "isVip": true,
      "refNum": "20200326gsj1d",
      "updatedAt": "Thu, 26 Mar 2020 05:57:41 GMT"
    },
    "satisfaction": {
      "createdAt": "Thu, 26 Mar 2020 05:57:41 GMT",
      "createdBy": 1,
      "id": 2,
      "isActive": true,
      "pledgeId": 2,
      "rating": 4,
      "updatedAt": "Thu, 26 Mar 2020 05:57:41 GMT"
    }
  },
  "status": "success"
}```
