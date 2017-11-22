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

3. Manually enter more data in firebase, this time under "messages" in order to group these messages into their corresponding room that would display when each room was clicked by the user. Use 'orderByChild()' method to identify the 'roomId' of each grouping to be able to pull each message grouping from firebase to its room on the homepage.

4. Create modal on '.run()' and store a username in the app's cookies.

5. Create text input to send message to active room corresponding to username, with timestamp, updating live.

## Solution

1. After manual data entry, created factory service called Room.js centered around '.child()' method to list rooms from firebase by index using simple function that returns array. Created a HomeCtrl.js to manage the '$scope' of the homepage with injected dependency of Room.js. Defined $state in app to use {{}} syntax in html. Defined some css to manage appearance and readability.

2. Created modal to animate open on button click for user to create room using '$uibModal' bootstrap method, stored created room info with '$log' method. Created modal instance controller to manage user input. Created a simple html document for the modal and styled with css.

3. After data input in firebase, added 'ng-click' method to add user functionality to the listed rooms. Used 'orderByChild()' to define each message set for each room. Styled the page to have the rooms listed on one side and the messages listed on the other.

4. Used '$cookies' to store a username on page open with '.ok()' method which would require the modal to stick until user inputs a value.

5. Created a send function in message service that would '.push' a message bound with the username and timestamp to the array in firebase, and would populate in the room's messages instantaneously. Bound username with stored cookies by injecting '$cookies' dependency and referencing the current user.

## Results
1. Display of Room List
{:.center}
![]({{ site.baseurl }}/img/room_list.png)

2. Room Creation Modal
{:.center}
![]({{ site.baseurl }}/img/create_room_modal.png)

3. Messages in Specific RoomI
{:.center}
![]({{ site.baseurl }}/img/bloc-chat.png)

4. Username Modal View
{:.center}
![]({{ site.baseurl }}/img/username_modal.png)

5. Send Message Input
{:.center}
![]({{ site.baseurl }}/img/send_message.png)

## Conclusion

This project was designed to "take the training wheels off" and though challenging proved to be very fun. The real challenge was making sure to console log my functionality so I could see where errors occured or didn't. Angular proves to be a bear but carefully linking the services and controllers proves it to be a very effective framework. Syntax has always been a struggle for me just with all the new terminology but I think it a small price to pay for mastery.
