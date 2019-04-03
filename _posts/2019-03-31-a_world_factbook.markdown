---
layout: post
title:      "A world factbook"
date:       2019-03-31 18:49:21 +0000
permalink:  a_world_factbook
---


My final project at Flatiron School was a react application with a rails API backend – I decided to do a world factbook.

## A map

Naturally; before going after any of the project requirements I decided to get a cool looking map on the page – so fresh! so international! To accomplish that; I used d3-geo + open source topojson data to place a SVG map with an orthographic projection that rotates when you drag it. The front page also includes a react-autosuggest searchbar for easily looking up countries.

## A Country

After selecting a country, the application redirects to the country's page; which requests an excerpt about the country from the wikipedia API as well as reloading the map component (now centered on the selected country) and rendering an SVG of the country flag.

## Foreign Exchange

On the country page is another country searchbar; if you select a country; it will take that country and send pertinent info to the rails API; which will call a currency exchange API and then save the search and return the result. previous currency exchange searches are displayed on the page.
