---
layout: post
title:      "Reflections on The Coming Software Apocalypse"
date:       2018-05-10 14:42:04 +0000
permalink:  reflections_on_the_coming_software_apocalypse
---


I read an excellent article in The Atlantic, [The Coming Software Apocalypse](https://www.theatlantic.com/technology/archive/2017/09/saving-the-world-from-code/540393/) that I have not been able to stop thinking about especially as I have progressed into building more complex models and associations using ActiveRecord and Sinatra.

The article talks about the overwhelming complexity of the systems we are building and the system errors that are created when the human behind the machine is not able to process the entire scope of what they are building much less the problem they are trying to solve. Software developers are abstracted away from the real life work their software is designed to execute and so may not be able to easily understand the ramifications of their programming choices. Once a program becomes millions of lines of code, it becomes impossible for any one person to truly visual the flow of logic through the entire system. 

The things I have been building, by the above standards are incredibly simple. Yet, I can already feel the limit of my ability to hold the system in my mind being tested. I find I am able to solve problems by simply walking through the code less efficiently and rely much more on tools like Capybara tests, Shotgun, and Pry to actually run the code and make sure things are behaving as expected. Yet these are imperfect as well- I have used shotgun to load my app in the browser and have everything appear on the surface to be functioning as expected, yet behind the scenes my data was being saved incorrectly. 

I formerly studied Human Factors Psychology, which I like to sum up as the study of designing systems to work with the limitation of the human brain. It is clear to me that programming has a major human factors problem. The capabilities of what we are able to create have way out paced our ability to understand them. 

I am extremely intrigued by the idea of model-based design. I absolutely believe that programming tools rather than products makes the most sense. Everything is becoming code, but not everyone will learn to code, and those of us who love it can build the tools that make development accessible and more human centered.
