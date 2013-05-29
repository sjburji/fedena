fedena
======

Code base adopted from Fedena open source - https://github.com/projectfedena/fedena

Installation instructions (*nix based OS preferred for dev)
=========================

1. use git link - git@github.com:sjburji/fedena.git
	
	or 
	
	unzip from here - https://github.com/sjburji/fedena/archive/master.zip

2. The working folder should be fedena-master

3. fedena/config/database.yml is the database connection settings
   - Currently it uses mysql with "root" user and "" passwaord (yes no password)
   - dev db is fedena
   - update username and / db as necessary for "development"

4. On the command line $
	 - check for ruby version, 1.8.7-p302 is preferred, later versions are not supported
	 - if you are behind a proxy server : use export http_proxy=username:password@192.168.2.38:3128
	 - check if you have bundler using 
	 			$ bundle install 
	 			else
	 			$ gem install bundler
	 - bundle install
	 - rake db:create
	 - rake db:migrate
	 			- if you run into versions requirement errors then
	 				running the following commands can resolve it:
					$ gem install rubygems-update -v='1.4.2'
					$ update_rubygems
	 - rake fedena:plugins:install_all

5. To run the dev server at command line $
	 - script/server

6. To run the web application in the browser - use http://localhost:3000

7. Demo seed data will give you the following -
	* As admin -- username - admin, password - admin123
	* As student -- username - 1, password - 1123
	* As employee -- username - E1, password - E1123
