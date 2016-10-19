# Twilio Voting System

This project uses [Twilio](https://www.twilio.com) on [Google App Engine Flexible Environment](https://cloud.google.com/appengine).

For more information about Twilio, see their [Python quickstart tutorials](https://www.twilio.com/docs/quickstart/python).

## Setup

Before you can run or deploy the sample, you will need to do the following:

1. [Create a Twilio Account](http://ahoy.twilio.com/googlecloudplatform). Google App Engine
customers receive a complimentary credit for SMS messages and inbound messages.

2. Create a number on twilio, and configure the voice request URL to be ``https://your-app-id.appspot.com/call/receive``
and the SMS request URL to be ``https://your-app-id.appspot.com/sms/receive``.

3. Configure your Twilio settings in the environment variables section in ``app.yaml``.

## Running locally

Create and activate the virtual environment

    $ virtualenv env --python=python3
    $ source env/bin/activate

Install the dependencies

    $ pip install -r requirements.txt

You can run the application locally to test the callbacks and SMS sending. You
will need to set environment variables before starting your application:

    $ export TWILIO_ACCOUNT_SID=[your-twilio-accoun-sid]
    $ export TWILIO_AUTH_TOKEN=[your-twilio-auth-token]
    $ export TWILIO_NUMBER=[your-twilio-number]
    $ python main.py
