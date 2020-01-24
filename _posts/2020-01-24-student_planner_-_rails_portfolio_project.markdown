---
layout: post
title:      "Student Planner - Rails Portfolio Project"
date:       2020-01-24 22:06:59 +0000
permalink:  student_planner_-_rails_portfolio_project
---


Where do I even begin, this project was a beast! It definitely flexed a lot of the Rails muscles we learned over the course of this module and to have finally completed it feels very rewarding. Shortly after I began my project I faced some monumental life changes and some health issues which forced me to sideline my progress for a while. This break definitely taught me the value of getting some coding in daily, because when I returned to my project I found myself frequently going back to look at past lessons for review. All is well that ends well though, and I am proud of what I've accomplished.

I chose to create a Student Planner application that allows a student to create a profile, view their schedule, add/edit/delete courses on their schedule. Additionally students are able to view current assignments and assignments that are due soon, as well as the ability to add/edit/delete assignments. 

One thing in particular that I struggled with was when it came time to implement a social login feature. I chose to use Google, which was fairly straightforward until I was trying to `find_or_create_by(id: auth['id'])`. The first issue with this I learned was you don't want to ever assign the id yourself, as it should always be done by the database when an object is created. To remedy this I added another attribute to the Students table called 'uid' and then I used `find_or_create_by(uid: auth['uid'])`. 

I was getting close, but now I was getting an error I wasn't familiar with, a Range Error. 
The error read: `116403713997777988489 is out of range for ActiveRecord::ConnectionAdapters::SQLite3Adapter::SQLite3Integer with limit 8 bytes`. I went into detective mode and scoured Google for potential solutions, but most hits were talking about moving the default limit of 4 bytes to 8, which wouldn't help me. Eventually I found a solution in the form of changing the 'uid' attribute from an integer to a string, which worked perfectly! 

Overall I think this will be a great addition to my portfolio, though going forward I think I would like to make the application a little more visually appealing with some additional CSS.
