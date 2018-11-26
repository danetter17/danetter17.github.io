---
layout: post
title:      "My First CLI Data Gem"
date:       2018-11-26 21:02:15 +0000
permalink:  my_first_cli_data_gem
---


The thought of building something entirely from the ground up was something that both excited and terrified me at the same time. Starting with a blank canvas seemed so daunting, but upon completion of this first project was incredibly rewarding. To see the hours of work culminate into a functioning, interactive CLI program was a huge milestone. 

The name of my CLI Gem is **illinois-colleges** and it features:
* An interactive CLI interface found within the cli.rb file
* A scraper class that is found within the college.rb file
* Two levels of information: the name of every college in the state of Illinois, and once selected, its location

To interact with the program, you must first run `git clone git@github.com:danetter17/illinois-colleges.git` in your terminal. You will then want to change directories into the 'illinois-colleges' directory with `cd illinois-colleges`. Follow this with `bundle install` to finish the installation. From here you can run the program with `ruby bin/illinois-colleges`.
Once in the program you will be met with a welcome message that lists your options: `list` to provide a numbered list of each of the colleges, or `exit` to exit the program. If the user enters 'list' then they are prompted to select the number of the college or university they would like more information on, which is then displayed to the user. 

The most time consuming step of this project was definitely setting up the scraper class correctly, but with the help of binding.pry and Nokogiri I was able to inspect the various searches I was performing. What I ended up with looked something like the following: 
`doc.xpath("//tr").each do |doc|
      college = self.new
      if doc.css("td")[0] != nil
        college.name = doc.css("td")[0].text.strip
      end`

Overall this project was an excellent learning experience that really pushed me to see what I was made of. There were definitely points that I was frustrated but in the end, it was well worth the feeling of accomplishment. In the future, I would like to continue adding to the program to scrape a second webpage that contains additional details.





