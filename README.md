# Project 8 - Pentesting Live Targets

Time spent: **5** hours spent in total

Vulnerbility 1: (Green) Username enumeration is in this part of the site. "Log in was unsuccessful." shows as bold whenever the account exists, and not bold if it does not exist.
http://imgur.com/WVU9hcY

Vulnerbility 2: (Red) The Find a Salesperson site uses GET params to get the id of the salesperson. Changing the number gives a different sales person, so if we tried to get 10 on the red site, it gives us a salesperson who was not supposed to be released yet. The other 2 sites makes a check on whether or not that salesperson would be allowed to be viewed, and if not, it redirects to territories page.
http://imgur.com/EgefySC

Vulnerbility 3: (Blue) Also in Find a Salesperson, if you pass in the SQL injection into the id param, it makes the site sleep for 5 seconds before reloading. Using ' OR SLEEP(5)=0--' works.
http://imgur.com/fXu3ahO
