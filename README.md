Running Faye Server on Heroku Cedar stack
=========================================

Clone respository
-----------------

Change to your directory:

    cd app_directory

eg:

    cd my_faye_server

Clone from GitHub:

		git clone git://github.com/TsaiKoga/

Initializing git
-----------------

Initialize git:

		git init

Creating a new app on Heroku
---------------------------

Install Heroku gem if you don't have already installed it:

    gem install heroku

Creating a this app on Cedar stack:(you can write app name by yourself)

    heroku create private_pub-heroku-cedar --stack cedar

So your app name will be private\_pub-heroku-cedar on heroku.

Change the Config:
-----------------

You can see there is a file 'config/private\_pub.yml',you must change the production server like below:

    server: "http://private_pub-heroku-cedar.herokuapp.com/faye"

private\_pub-heroku-cedar.herokuapp.com is depend on your heroku app name.


Push code to Heroku
-------------------

Hand up your files:

   git add .

	 git commit -m"change config/private_pub-heroku-cedar"

Push these files to Heroku:

    git push heroku master

Go to you provided by Heroku link and check that your server is up add running!

Change your appilication that use this private\_pub-heroku-cedar
---------------------------------------------------------------

Change the links in your layout/application.html.erb and assets/javascripts/application.js

    http://private_pub-heroku-cedar.herokuapp.com/faye.js

    http://private_pub-heroku-cedar.herokuapp.com/faye

References
----------

- Faye - http://faye.jcoglan.com/
- Heroku - http://heroku.com

Special Thanks
--------------

- James Coglan - Faye Developer
- ntenisOT     - The Scheme
