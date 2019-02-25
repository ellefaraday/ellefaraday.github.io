---
layout: post
title:      "Rails, Resources, and Routes"
date:       2019-02-25 19:44:17 +0000
permalink:  rails_resources_and_routes
---


For my current rails project I decided to make something related to what I do at work. A time consuming part of my job is organizing volunteers to help out for different activities at our non-profit. I have tried a number of technical solutions including, email, google forms, and signupgenius.com to help coordinate volunteers. Because nothing perfectly meet our needs, we have settled on a hodgepodge of the above. So, I decided it would be interesting to start building a Volunteer Coordinator App.

The app has two main models, users and time slots. There is a third model that operates as a join, user time slots, to support a many to many relationship. I wanted volunteers to be able to sign up for multiple time slots and for time slots to have multiple volunteers. So far so good.

For this project I also made use of nested resources to keep a logical connection between the volunteer and the time slots they signed up for following RESTful conventions. For example when a user chose to view the time slots they signed up for the url would be /users/user_id/time_slots rather than the less specfic /time_slots. This lead me to some difficult decisions and some unexpected behaviors.

Previous to this project, I had found following RESTful and MVC conventions fairly straight forward. Actions associate with the user went in the user controller and actions associated with time slots went in the time slots controller — all fine. But what about when a user signs up for a time slot? At first I put this action in the time slot controller under the new action, however, creating a new time slot was not actually the same thing as a user signing up for a time slot. Signing up for a new time slot actually involved accessing the join model user time slots. Still, with my nested routes, I was routing through users/user_id/time_slots/new and that seemed pretty clearly to point to the time slots controller. I ended up with a bloated new action and view that served up a different form whether it was accessed via time_slots/new or users/user_id/time_slots/new. This didn’t feel quite right, but I let it be.

The next issue I ran into was some unhelpful route helpers. I had lazily requested all resources for my 3 models as well as my nested resources in my routes.rb file when I first started sketching things out, unsure of what I would actually need. As I was building things out I tried to use the helper user_time_slots to get to user/user_id/time_slots, but I was getting weird bugs. What the heck? Rake routes helped me uncover some unexpected behavior. Because I had requested resources for the join class user time slots first before I put in the nested routes, the helper user_time_slots was assigned to the url user_times_slots/index not user/user_id/time_slots

I discovered that by switching the order, I switched the priority and the helpers would be assigned to the nested routes, or I could delete the user time slot routes all together if I wasn’t going to use them. I couldn’t quite get past the feeling that there ought to be a separation of concerns for what belonged to the time slots controller and that it was pulling double duty with my current solution.

Ultimately, I decided to refactor and keep user time slot routes for new and edit. This allowed me to pull the sign up form out of the new time slot action and view and give it it’s own action and view in the user time slots controller. It felt a lot more clean and clear. I allowed user time slots to keep the priority in routes so that it would get the named helpers and just use the long form of the url paths wherever I needed the nested resources.

I am not sure if what I chose is the recommended solution. It felt like the truest adherence to separation of concerns to me. I feel like I learned a lot about the nitty gritty architecture choices that have to be made once things become complex. The patterns certainly help, but I understand them more now as guiding principles rather than rules that can always be applied perfectly.
