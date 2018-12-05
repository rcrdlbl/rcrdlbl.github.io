---
layout: post
title:      "A calorie tracker built in rails"
date:       2018-12-05 18:51:26 +0000
permalink:  a_calorie_tracker_built_in_rails
---

For my Flatiron school rails unit project, I made the decision to create a web app that allows users to track the things they've eaten and how much calories they contain, and see if they've eaten more than their designated calorie limit for the day; as well as tracking how different food items make them feel.

### The Process
After first writing down how the database model structure would work, I ran generators to create the database tables and the corresponding empty rails model files. I then installed the `oauth` and `oauth-facebook` gems to enable facebook login capability and set up the cryptographic keys using the facebook developer website. Afterwards I set out first creating the user sign up, login, and profile pages. Afterwards I worked on making sure users could create food items and append a calorie count to each food item. I then created a join table between users and food items called meals. A user could then use a nested new route under food_items to create a meal, which then could be seen under a nested index and show route under user. The meals also have a scope item called eaten_today, which displays all the meals eaten today. This is called on by the user's profile page to display the calorie count of all meals the user has eaten that day. 
After this, I created validations for various attributes (no negative calorie foods, guys!)

On a whim I decided to style the application even though it wasn't required, so I put the bootstrap stylesheet in the main application and placed all UI elements within bootstrap's card UI, and set the links within the application to appear as bootstrap's native button design, with the index pages displaying as bootstrap's styled list, creating an understandable look for the project.

[View the project on github](https://github.com/rcrdlbl/calorie-tracker)
