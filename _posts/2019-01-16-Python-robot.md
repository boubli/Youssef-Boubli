---
layout: article
title: "Texting robots on Mars using Python, Flask, NASA APIs and Twilio MMS"
date: 2019-01-15 19:45:00+0200
coverPhoto: https://s3.amazonaws.com/com.twilio.prod.twilio-docs/images/NASA_Mars_Rover.width-808.jpg
---

![](https://s3.amazonaws.com/com.twilio.prod.twilio-docs/original_images/h8izjko1F-KJd0nWj0DcJF3vJ81Fk5wGhd1d3eRE38V9AqDua1SIQWIuicJf_LwtNsJVQfOCN_.png)

NASA has a bunch of awesome APIs which give you programmatic access to the wonders of space. I think the Mars Rover Photos API in particular is really amazing as you can use it to see what kind of pictures the Mars Curiosity rover has been taking.

Let’s build an app using the Mars Rover API with Twilio MMS, Python and Flask to make it so that we can text a phone number and receive pictures from Mars.

Setting up your environment
Before moving on, make sure to have your environment setup. Getting everything working correctly, especially with respect to virtual environments is important for isolating your dependencies if you have multiple projects running on the same machine.

You can also run through this guide to make sure you’re good to go before moving on.

# Installing dependencies
Now that your environment is set up, you’re going to need to install the libraries needed for this app. We’re going to use:

 *Flask for our web framework
 *Requests to grab data from the Mars Rover API
 *Twilio’s Python library to interact with the Twilio API.

Navigate to the directory where you want this code to live and run the following command in your terminal with your virtual environment activated to install these dependencies:

```cmd
pip install requests==2.13.0 twilio==6.0.0 flask==0.12.1
```

# Requesting data from other APIs
Let’s start by writing a module to interact with the Mars Rover API, which is a URL that returns some JSON.
Create a file called `mars.py` and enter the following code:

```python
	import requests
	from random import choice

	rover_url = 'https://api.nasa.gov/mars-photos/api/v1/rovers/curiosity/photos'

	def get_mars_photo_url(sol, api_key='DEMO_KEY'):
	    params = { 'sol': sol, 'api_key': api_key }
	    response = requests.get(rover_url, params)
	    response_dictionary = response.json()
	    photos = response_dictionary['photos']

	    return choice(photos)['img_src']
```

What we’re doing here is sending a request using the `requests` module to the URL corresponding to Mars Rover’s API, parsing the JSON response, and grabbing the URL associated with a random image for whatever Martian Solar day we provide.

![](https://s3.amazonaws.com/com.twilio.prod.twilio-docs/original_images/h8izjko1F-KJd0nWj0DcJF3vJ81Fk5wGhd1d3eRE38V9AqDua1SIQWIuicJf_LwtNsJVQfOCN_.png)

# Setting up your Twilio account
Before being able to respond to messages, you’ll need a Twilio phone number. You can buy a phone number here.

Your Flask app will need to be visible from the Internet in order for Twilio to send requests to it. We will use ngrok for this, which you’ll need to install if you don’t have it. In your terminal run the following command:
```python
	ngrok http 5000
```
![](https://s3.amazonaws.com/com.twilio.prod.twilio-docs/original_images/hmTx20qaRj5weu107nZN_03ey5GtE_gfhZL38JxTpVLVTpL23suwFAKp2oC1rifmb44EuxFjAe.png)

This provides us with a publicly accessible URL to the Flask app. Configure your phone number as seen in this image:

![](https://s3.amazonaws.com/com.twilio.prod.twilio-docs/original_images/0aSHD86LufqYSUxH8tpXT9qMUwxFTNtRywL7JmqAtHUnAtByJp5NXL_xVOeN2exR9DLpPn3Thf.png)

You are now ready to [send a text message](https://www.twilio.com/blog/2017/04/texting-robots-on-mars-using-python-flask-nasa-apis-and-twilio-mms.html) to your new Twilio number.

# Building the Flask app
Now that you have a Twilio number and are able to grab a URL corresponding to an image taken on Mars, you want to allow users to text a phone number to view these images.

Let’s create our Flask app. Open a new file called `app.py` and add the following code:

```python
	import os

	from flask import Flask, request
	from twilio.twiml.messaging_response import MessagingResponse, Message

	from mars import get_mars_photo_url


	app = Flask(__name__)


	@app.route('/sms', methods=['POST'])
	def inbound_sms():
	    message_body = request.form['Body']
	    resp = MessagingResponse()

	    if message_body.isdigit():
	        response_message = 'Taken {} Martian solar days into the journey.' \
	                           .format(message_body)
	        photo_url = get_mars_photo_url(message_body)

	        msg = Message().body(response_message).media(photo_url)
	        resp.append(msg)
	    else:
	        msg = Message().body('Text a number of solar days into the rover\'s journey.')
	        resp.append(msg)

	    return str(resp)


	if __name__ == '__main__':
	    app.run()
```
We only need one route on this app: `/sms` to handle incoming text messages.

Run your code with the following terminal command:

```python
	python app.py
```
Now text your Twilio number to literally communicate with a robot on Mars!

# What just happened?
With this app running on port 5000, sitting behind our public ngrok URL, Twilio can see your application. Upon receiving a text message:

```cmd
	Twilio will send a POST request to /sms.
	The inbound_sms function will be called.
	A request to the Mars Rover API will be made, receiving a JSON response that then gets parsed to acquire an “img_src” URL to a photo from Mars.
	Your /sms route responds to Twilio’s request telling Twilio to send a message back with the picture we retrieved from the Mars Rover API.
```
