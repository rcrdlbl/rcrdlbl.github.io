---
layout: post
title:      "Calorie Tracker Update"
date:       2019-02-04 15:13:55 +0000
permalink:  calorie_tracker_update
---


The Rails/JS portfolio project section of my course involved taking my previous Rails project and incorporating JQuery and ActiveModel Serializers to dynamically render content on the page via JQuery AJAX requests.

The first step I took was creating serializers within activemodel to return database information in JSON format, with an additional custom method in the meal serializer to determine if a user ate said meal today.

### Javascript Setup

The jquery in my application has 2 listeners set up to activate when the page loads, one checks to see if a food item is clicked on the food items index page; which then appends the form to create a meal onto the page, prefilled with the food item's ID and the user's ID. The second listener is set up to listen for the button itself being clicked, which sends a POST request to create a new meal, and afterwards replaces the meal form with the information related to the meal.

A second function is set up on document load, that obtains a list of meals the user has eaten that day and appends it to their profile page.

### Styling

Opening my project after a while away from it made me realize that the previous bootstrap style looked somewhat lazy, so I decided to remove all references to bootstrap from the original project and instead faithfully transfer the USDA's nutrition label style guidelines over to this project using CSS, which leads to a much more memorable look while making the site significantly more lightweight.

#### Project:
[Github](https://github.com/rcrdlbl/calorie-tracker/tree/js)
[Demo Video](https://youtu.be/WUxNs8jfPes)
