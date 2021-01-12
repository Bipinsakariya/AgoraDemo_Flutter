# AgoraDemo

## Video calling App using Agora SDK

	- Google Sign in
	- Firebase 
	- Agora.io SDK for Flutter (agora_rtc_engine)
	- Push Notification

# What 
  This app provides Video/Audio calling features on Peer-to-Peer or Peer-to-Many transaction, This transaction is dependent upon Agora SDK (agora_rtc_engine)      provided by Agora.io for Flutter. 

# Why : 
  Friction free engagement of our user to app is at almost importance, If our app has any social relations which involves individual or Group then having smooth  communication among them becomes top priority. 
Video/Audio calling provides quick interaction of users which results into healthy engagement towards our app.
Video/Audio calling becomes a must for situations like chat modules, streaming and group call/meetings.

# How : 
Set up a Flutter Project
# Firebase setup :
- Configure firebase to our project => firebase_core | firebase_auth | firebase_database
- Firebase Database (Saved data into realtime database)
- Name
- Email
- Image
- Token(FCM token for push notification)
# Google sign in setup :
- Configure Google Sign In =>  google_sign_in
- Google sign in will save users information to firebase database which will then used as uniqe identification for user and call them.
- Push Notification setup :
- Configure Push notification => firebase_messaging
- Push notification is used as to notify the user that someone is calling. Once user tap on the notification, user will be redirected to video calling (Joins the channel) screen.
- Push notification can only be received if app is in background or killed. When app is in foreground user is automatically redirected to video calling screen.
- Which persone to send notification for joining the video call will handled by the FCM token saved to that user in firebase database.
- We can send notification from app on user events using API call :- [ https://fcm.googleapis.com/fcm/send ]

# Agora SDK :
- Configure Agora.io SDK => agora_rtc_engine
- Generate an APP_ID by signing into Agora.io.
- Create a channel and get associated Token Id from Agora.io and store it into app. These three things will be used as a communication channel where user will join for call.
- User will be able to 
- Join / leave a channel
- Mute / unmute audio
- Switch camera views
- Layout multiple video views
