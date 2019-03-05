---
layout: post
title:      "Sinatra Portfolio Project: Bucket Lister"
date:       2019-03-05 00:10:01 +0000
permalink:  sinatra_portfolio_project_bucket_lister
---


For this assessment we were required to build a CRUD MVC application using Sinatra, a domain specific language built in Ruby. A CRUD MVC application denotes both the structure and the basic functionality the application with employ. CRUD points towards the functionality, standing for Create, Read, Update and Destroy. In other words, a user that is logged in should have the ability to create a new object (and persist it to the database), read (or view) that object, update that object (and persist this updated version to the database), and destroy/delete that object from the database. 

The project requirements were as follows:

1. Build an MVC Sinatra application.
2. Use ActiveRecord with Sinatra.
3. Use multiple models.
4. Use at least one has_many relationship on a User model and one belongs_to relationship on another model.
5. Must have user accounts - users must be able to sign up, sign in, and sign out.
6. Validate uniqueness of user login attribute (username or email).
7. Once logged in, a user must have the ability to create, read, update and destroy the resource that belongs_to user.
8. Ensure that users can edit and delete only their own resources - not resources created by other users.
9. Validate user input so bad data cannot be persisted to the database.
BONUS:  Display validation failures to user with error messages

Talk about a challenge!! This project really upped the complexity when compared to our first data-gem assessment, definitely a lot more moving pieces. Currently I believe I have stubbed out all of the required functionality and am working towards incorporating the 'rack-flash3' gem to display custom error messages. 

The basic premise of my application as the name implies is to build a personal bucket list. After signing up with a unique username a user can create, read, edit and delete any item that they have created. A challenge I faced early on while getting started was getting my environment built out correctly. After struggling for a while I came across a useful little gem called 'Corneal'. What a lifesaver! This gem builds out a simple backbone to get a basic Sinatra app up and running (wish I had known about this earlier!!). The challenge I am currently facing involves making the application more visually appealing, which I plan to tackle once I have a better understanding of more front-end technologies. Overall this was a great challenge and I look forward to working on this application again in the near future!!


