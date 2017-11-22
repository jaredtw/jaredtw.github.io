---
layout: post
title: Bloc Chat
thumbnail-path: "img/bloc-chat.png"
short-description: Create a chat app for creating rooms and sending messages

---

{:.center}
![]({{ site.baseurl }}/img/bloc-chat.png)

## Explanation

This assignment was an introduction to using a real-time database(firebase) to store and display data. Along with what I learned about AngularJS, I used new parameters like $cookies and $uibModal in my angular services as well as $log and $uibModalInstance in my controllers.

## Problem

1. Mock-up data in firebase to display using 'firebase.database().ref().child("rooms")' and create a factory service to provide this data to index.html. Then create a controller to manage the home page.

2. Create a modal to add rooms to the firebase array using 'add' method in the room service, which requires two controllers: one to pop up the modal, and one to manage the user's actions on the modal. Use UI Bootstrap as a dependency to use '$uibModal' method.

3. Manually enter more data in firebase, this time under "messages" in order to group these messages into their corresponding room that would display when each room was clicked by the user. Use 'orderByChild' method to identify the 'roomId' of each grouping to be able to pull each message grouping from firebase to its room on the homepage.

4. Create modal on '.run()' and store a username in the app's cookies.

5. Create text input to send message to active room corresponding to username, with timestamp, updating live.

## Solution


## Results


## Conclusion
