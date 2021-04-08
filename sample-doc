# Project 2 API Documentation

The format of this API documentation was based on [RestApiDocs Example](https://github.com/jamescooke/restapidocs). You may also get endpoints information from our [postman doc](https://documenter.getpostman.com/view/2708935/SzYT62ek?version=latest). 

**Note**: 
*  - [ ] - endpoint has not yet been implemented
*  - [x] - endpoint implementation is finished

## Session Management Endpoints

We use Firebase for handling our API auth service you can check it [here](https://console.firebase.google.com/u/0/project/upbayanihanna/settings/iam). Basically, we use the `token` returned by a call to `signup` and `login` and attached it as an `Authorization` header to all protected endpoints.

Note that the validity of a `token` is just an hour, after which you call the `refresh_token` endpoint to get a new `token`.

* - [x] [Sign up](session/signup.md) : `POST /auth/signup`
* - [x] [Login](session/login.md) : `POST /auth/login`
* - [x] [Refresh Token](session/refresh-token.md) : `POST /auth/refresh_token`

## Endpoints that require Authentication

Closed endpoints require a valid Token to be included in the header of the
request. A Token can be acquired from the login view above.

### Pledges Endpoints

Endpoints for registering and listing pledges. 

 * [Register a pledge](pledges/register-pledge.md) `POST /pledges/`
 * [List of pledges](pledges/list-pledges.md) `GET /pledges/`
 * [Get a pledge by id](pledges/get-a-pledge-by-id.md) `GET /pledges/:transaction_id`
  
### Donations Endpoints

Endpoints for registering and listing donations.

 * [Register a donation](donations/register-donation.md) `POST /donations/`
 * [List of donations](donations/list-donations.md) `GET /donations/`
 * [Get donation by id](donations/get-a-donation-by-id.md) `GET /donations/:transaction_id`
  
### Disbursements Endpoints

Endpoints for registering and listing disbursements. 

 * [Register a disbursement](disbursements/register-disbursement.md) `POST /disbursements/`
 * [List of disbursements](disbursements/list-disbursements.md) `GET /disbursements/`
 * [Get disbursement by id](disbursements/get-a-disbursement-by-id.md) `GET /disbursements/:transaction_id`
