---
layout: post
title:      "Vitamin Notes"
date:       2018-10-12 20:33:45 +0000
permalink:  vitamin_notes
---


This project developed for my programming bootcamp is a web app that allows you to write down the vitamins you are taking and publish them. Users can then see vitamin recommendations from the community and after trying them, can post notes about their experience with a vitamin.

This application was made using sinatra to handle routing and activerecord to store information, as well as bcrypt to encrypt user login info.

The application files are split into models/views/controllers/helpers. Models contain the data structure and allow activerecord to interface with ruby. Views are all ERB(embedded ruby) files, which allow me to import ruby logic into HTML, allowing for dynamic web interfaces. The controllers take a web route as input, for example `something.com/login` would be set up to load the erb file login page, with another controller action that takes care of what the application does after clicking the login button. Helper files contain various methods that are used in the controllers, mainly for user validation in this case.

[Link to the project](https://github.com/rcrdlbl/vitamin-notes)
