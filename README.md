# Linux Server Deployment on AWS
The final project  has been created on AWS Lightsail.
The IP of the server is 13.58.102.62
The URL to the server is http://davidbarber.hopto.org/


# users
a user with the username of 'grader' has been created with sudo privileges
postgres - user for the postgresql database
catuser - user for the catalog postgresql database
webuser - user for postgresql database


# SSH
ssh has been disabled for root
ssh is only allowed using authorized public key
Login to the server using SSH as follows:
ssh grader@13.58.102.62 -p 2200 -i <path to key file>
OR
ssh grader@davidbarber.hopto.org -2200 -i <path to key file>
Key is provided with the project submission


# configurations
AWS firewall allows access to the following:
http (port 80 and 8080)
ssh (port 2200)
NTP (port 123)
All packages have been updated to current versions
Ubuntu is version 16
for the catalog application python version 2.7 is used in order to match the Udacity course
unattended-upgrade is setup.


# catalog application
to run the catalog application navigate to the url
http://davidbarber.hopto.org/
The catalog application uses a postgresql database.
you may login to the webapplication by clicking the 'login' link
at the top of the page to create your own categories, or just browse if you  do not want to login.
In order to make the login functional, I had to create a dynamic dns using hopto.org
because the Google OAUTH did not work for an IP address, but rather needed a domain name



# sample Postgresql database
# to prove that the Postgresql database is functional
ssh in as grader (see above)
type sudo su postgres
type psql at the prompt
type \c newDB
you should now be connected to the sample postgresql database
type select * from users;
you should see a row of data from the users table.


# third party sites used to assist in the project
Postgresql:
http://www.postgresqltutorial.com/postgresql-create-table/
https://wixelhq.com/blog/how-to-install-postgresql-on-ubuntu-remote-access
https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-18-04
http://www.postgresqltutorial.com/postgresql-python/connect/
https://suhas.org/sqlalchemy-tutorial/\
https://docs.sqlalchemy.org/en/13/core/engines.html#postgresql

apache web server:
https://help.ubuntu.com/lts/serverguide/httpd.html
https://www.jakowicz.com/flask-apache-wsgi/


Google OAUTH:
https://stackoverflow.com/questions/36020374/google-permission-denied-to-generate-login-hint-for-target-domain-not-on-localh/36162748#36162748
https://knowledge.udacity.com/questions/21110


To make catalog app run on server:
https://stackoverflow.com/questions/1518729/change-sqlite-database-mode-to-read-write
Https://knowledge.udacity.com

