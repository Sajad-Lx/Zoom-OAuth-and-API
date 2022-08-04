# Zoom OAuth and API
This repo is created to provide Zoom OAuth and API classes in python.
Not all APIs of Zoom are created here. If you need any API of Zoom, then you can go to their document and create a new API. Also, you can get idea of how to create API from my code.

## Requirments
- OAuth app from Zoom marketplace
- client_id from Oauth app
- client_secret from Oauth app
- redirect_uri to where it will redirect.

Both redirect_uri and allowed url should me mentioned in Oauth app.

## Zoom OAuth
For getting access_token at first time you need to get authorization code from Zoom and pass it to:

> ZoomOAuth().get_first_token(code)

Then, it will return a response which will have refresh_token. You have to store refresh_token for further API calls.

For getting authorization code, direct the user to https://zoom.us/oauth/authorize

**Example**

```https://zoom.us/oauth/authorize?response_type=code&client_id=7lstjK9NTyett_oeXtFiEQ&redirect_uri=https://yourapp.example.com```

For every API call you have to update old refresh_token to new token.

Feel free to add or change code and leave grammatical mistakes in document (👉ﾟヮﾟ)👉
