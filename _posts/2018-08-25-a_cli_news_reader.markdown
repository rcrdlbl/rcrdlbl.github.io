---
layout: post
title:      "A CLI News Reader"
date:       2018-08-25 14:56:06 +0000
permalink:  a_cli_news_reader
---


I've created an application that lets you access [tldrworldnews.com](https://tldrworldnews.com/), a website that offers quick summaries of the most important news stories from around the world. My original plan for this project was something that allowed you to search various food items on amazon.com, ranked by value (defined as calories per dollar), I was told that this was far too complicated however.

### Scraping

After doing the basic setup of requiring nokogiri, I found that the articles were encased in a div with the class 'listing'. I had the scraper class retrieve all of them, then iterate over them and pass each one along to the article class, which then proceeded to create a new instance of itself for each article. The html/css on the site was actually rather clean and uncomplicated, allowing me to focus on the more difficult portion, which was working out logic for the CLI.

### CLI Interface

I ended up with a CLI class containing 5 functions, including a start function that encapsulated the other functions, placing them within a logical order, plus prompts for action. It lists headlines, asks which article you'd prefer to read, displays the article, and asks if you'd like to read another, afterwards either repeating the process or exiting the application.

### Links
[The project repository on github](https://github.com/rcrdlbl/tldr-news)

[The gemfile on rubygems.org](https://rubygems.org/gems/tldr_news)
