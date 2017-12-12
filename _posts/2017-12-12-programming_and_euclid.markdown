---
layout: post
title:      "Programming and Euclid"
date:       2017-12-12 20:22:40 +0000
permalink:  programming_and_euclid
---

There are few exercises I have enjoyed more than working through the Book I of Euclid's Elements. With Euclid, you start out with a few tools that seem meager at first. You have 23 definitions, for example the definition of a circle or a triangle, 5 common notions such as "Things which equal the same thing also equal one another.", and 5 postulates which you must agree to use. 

These are the tools that Euclid starts you off with which are sufficient to build the first proposition. Each proposition starts with a task of what you are trying to do, and using your tools, contains the logic used to reach that goal. Each proposition has some givens or inputs and reaches a determined output. Once a proposition has been proven, it gets added to your tool box, you never again have to right out all of the logic for prop 1, you can reference it to work on future propositions and in this way Euclid builds through small managable blocks into a description of complex geometrical descriptions.

Euclid is beautiful. Euclidean geometry had remained in use for over 2000 years with little change and continues to be the foundation for how we desribe spatial relationships (non-euclidean geometry is equally interesting but perhaps a topic for another post). The logic of Euclid is so beautiful that it has often been referenced by philosophers as an exemplar of reaching a higher truth. Decartes sought to prove the existence of god with the same self evidence as mathematical truth. 

I have found, coding is beautiful too (maybe some languages more than others, I am currently loving Ruby and so will refer to Ruby specifically). Perhaps it seems strange to compare something as ephemeral as code, where languages seem to have the lifecycle of a gadfly to the ancient redwood that is Euclid. However, the system of though required for both flows from the same principles of logic and thought.

Ruby too begins with a set of tools: data types and methods. Like points, lines, triangles, and circles, the data types booleans, strings, integers, floats, arrays, and hashes are the small building blocks for your creations. Methods, like postulates allow us to act on our datatypes. 

As in Euclid reuseability it key. Once we have built a method, we add it to our tool chest to be called at need as we build increasingly complex methods. This is one of the main tenants of the underlying system of thought. For Euclid, once we have proved something it is forever accessible, we don't need to repeat the logic each time we want to refer to it in a proposition. This is key to allowing us to understand complex ideas. The 48th proposition, or Euclid's proof of the pythagorean theorem, references 4 other propositions, those 4 reference 10 other propositions, those 10 reference other propositions and so on until you can imagine how impossible it would be to place all of the logic require for proposition 48 in one block and have it be at all understandeable. 

Similarly, the reusability of methods in Ruby saves us not only the time for rewriting blocks of logic, but makes complex processes understandable to a human. Code must be legible by the computer, but ultimately, it must be legible by humans too if it is to be of use to us. 

Another key tenant that Ruby and Euclid have in common is abstraction. Abstraction in Euclid and programming, is probably the most jarring paradigm shift that new learners need to come to terms with. We begin learning math (and so logic) through specifics 2 + 2 = 4, not a + b = c. Euclid's Elements however, when it refers to a triangle, never refers to any specific triangle, but triangles in general. It is difficult for our brains to imagine a triangle as a concept devoid of instanitated attributes like side length, however, it is this abstraction, that Euclid's propositions prove something true not for 1 triangle in particular, but all triangles, which gives it the ultimate feeling of truth. Similarly it can be difficult to conceptualize the class itself versus an object which is an instantiation for a class. Once, objects can be thought about abstractly in the form of a class, however, it opens up a whole world of possiblilities for creating connections.

Good object oriented programming, like Euclidean geometry, feels beautiful. It is certainly worth the initial challenges of understanding. If taught well, both of the subjects provide the learner, not just with particular skills or knowledge, but with a pattern of thinking which is invaluable.



