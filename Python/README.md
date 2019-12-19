# Setup Requirements
In order to be able run an example you will need access to a cloud or on premise ams-mft login. If you would like to explore either this RESTful API or the .NETClient and don't have access to a AMS-MFT account then please contact our support team who will be happy to arrange you a free account for your testing - support@ams-ltd.com.

## Modules
When setting up your MFT-API using Python, we recommend the 'Requests' module is used.
This can be easily installed using pip, using the following command:

`pip install requests`
### Troubleshooting
If this command is 'not found' then attempt to locate your python environment and navigate to the 'Scripts' directory. The default Scripts directory location for python 3.6 onwards is as follows, depending on your operating system. Once inside the directory run the corresponding command to install the 'Requests' Module.
#### Windows:
Loction: `C:\Users\<user>\AppData\Local\Programs\Python\Python(xx-xx)\Scripts`

Command: `pip.exe install requests`
#### Linux / MacOS:
Location: `/usr/bin/python/Scripts`

Command: `./pip.exe install requests`

## Authentication
To Authenticate, each request must include a custom header which includes 'Base64' encoded credentials. Due to the sensitivity of each header and its stored information, every request **MUST** be sent across 'HTTPS' to ensure the request is encrypted. **Base64 Encoding will not solely secure your credentials.**

Here is an example of a custom header with authentication information:

`headers = {'Authorization': 'Basic ',
	    'Content-Type': 'application/json'}`