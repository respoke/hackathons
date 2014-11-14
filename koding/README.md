#Respoke + Koding + You = Worldwide Communication

Congratulations on being accepted to take part in the world's first global virtual hackathon! We're really excited at the opportunity to help all the teams add real-time communications to their apps, something that we feel will truly keep things global and provide an amazing user experience!

##What is Respoke and how can it help?
[Resoke](http://respoke.io) is a platform created to help developers easily add real-time communication features to their applications. You'll notice I used the word "feature", and this is an important distinction as we think that communication should be a native part of every application and website, and not a just a separate tool. 

##How do you I use Respoke in my applications?
We currently offer a Javascript library that allows you to easily implement things like real-time voice and video, as well as messaging and data functionality into your applications.

##Let's see some examples!
Let's say you want to add **messaging** capability to your app (maybe for support purpose, maybe to allow your users to communication with each other). You can do this by connecting to Respoke and using the sendMessage method:

```javascript
// make an endpoint for that recipient
var endpoint = client.getEndpoint({ id: remote });

// grab the text to send
var messageText = $("#textToSend").val();

// send it
endpoint.sendMessage({ message : messageText });
```              

How about making an **Audio Call**?

```javascript
// Call somebody
$("#makeCall").click(function () {
    var endpoint = client.getEndpoint({ id: $("#remoteId").val() });
    call = endpoint.startAudioCall();
    call.listen('hangup', function () {
        call = null;
    });
});

// Hang up on them
$("#endCall").click(function () {
    if (call) {
        call.hangup();
        call = null;
    }
});
```

#How do I get started?
First thing you'll need to do is create a Respoke account. To do this, click the following link: [https://www.respoke.io/#join](https://www.respoke.io/#join/tailored-houndstooth-jacket) and enter your information in the signup form. After completing the form, you'll receive a confirmation email with a link to complete your registration.

After you're all signed up, head over to our [Quickstart Guide](https://docs.respoke.io/) for a fast run-down on getting started. You can also find lot's of useful information in our [Docs](https://docs.respoke.io/). 

#Good luck!
From the entire Respoke team, we want to wish you all the best of luck at the hackathon and can't wait to see what you build! 

