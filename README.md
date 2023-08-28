## Django Socket Authentication Example

This project demonstrates how to implement authentication in Django web sockets. It leverages Django Channels and Daphne to enable asynchronous responses, as Django doesn't support async responses by default.

## Features

* Custom Socket Authentication
* JSON Data Validation
* Endpoint for Real-Time Notification Triggers


## Usage

* Start by creating a virtual environment.
* In the project's root directory, run the following command to install the required dependencies:

```
pip install -r requirements.txt
```

This will ensure all the necessary requirements are installed.

First, get a token at the login endpoint where you send the user's email and password:
```
http://localhost:{port}/auth/login/
```

When connecting to the notification socket, remember to include the user's token in the header of your client request, using the "token" keyword.
Use this path to connect:
```
ws://localhost:{port}/ws/notification/
```

To trigger a notification, make a GET request to the notification trigger endpoint using the following endpoint:

```
http://localhost:{port}/auth/trigger_notifications/
```



