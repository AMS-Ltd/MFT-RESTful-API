# Setup Requirements
In order to be able run an example you will need access to a cloud or on premise AMS-MFT login. If you would like to explore either this RESTful API or the .NETClient and don't have access to a AMS-MFT account then please contact our support team who will be happy to arrange you a free account for your testing - support@ams-ltd.com.

## Modules

## Authentication
To Authenticate, each request must include a custom header which includes 'Base64' encoded credentials. Due to the sensitivity of each header and its stored information, every request **MUST** be sent across 'HTTPS' to ensure the request is encrypted. **Base64 Encoding will not solely secure your credentials.**

The credentials must be Base64 encoded as `Username:Password` before being added to the header.