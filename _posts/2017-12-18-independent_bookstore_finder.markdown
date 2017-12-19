---
layout: post
title:      "Independent Bookstore Finder"
date:       2017-12-19 01:59:16 +0000
permalink:  independent_bookstore_finder
---


For my Object Oriented Ruby project I created a gem that scrapes the [New Pages](http://www.newpages.com/independent-bookstores) independent bookstore directory. 

Through a CLI users are able to select a state then see a list of cities in that state that have independent bookstores. Users next select the city they wish to view and are provided with the stores in that city. Finally, users can choose a bookstore to find out additional details about that store. 

Conceptualizing and coding this project made me more than ever an accolyte of object oriented programming. The multiple menus and relationships between states, cities, and stores could have felt daunting but I was able to break it down to a few straightforward relationships between each class type: states have many cities, states have many bookstores through cities, cities belong to a state and have many bookstores, a bookstore belongs to a city.

Another method I found incredibly helpful for simplifying the coding process was building it very chronologically through the user experience and stubbing out the flow before ever actually implementing the specific code. It made it very simple to see what data I needed at any give place in the program and how my methods would fit together. Ultimately I was able to code out my program in this way and have very little need to debug in order to get it all working.

Without this framework of approaching the problem, it could have been quite difficult to connect all the pieces together. Instead, they fit together naturally, as each subsequent piece was built to connect to what came before and to deliver what would be needed next. 

It was incredibly rewarding to create my first independent project without any scaffolding. I feel a renewed sense of confidence in my ability to break down complex problems and implement solutions. I can't wait to do the next one!

If you would like to check out my gem you can find instructions [here](https://github.com/ellefaraday/indie-bookstore-finder).
