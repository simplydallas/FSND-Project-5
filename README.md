##### Web view of the hosted app:
* [http://52.26.132.12/](http://52.26.132.12/)

##### login:
* ssh -i udacity_key.rsa grader:project5@52.26.132.12 -p 2200
* note: replace udacity_key.rsa with the path / name of the actual rsa file

##### Changes made:
* installed apache, postgresSQL, mod_wsgi, git, and all required files for catalog app
* configured firewall to block all ports other than 2200, 123, and 80
* set timezone to UTC
* changed SSH port to 2200
* added user grader, enabled sudo, set password to project5, and added ssh keys to the user
* added user catalog, set them up with limited permissions with psql

### Some notes about changes made above the stated requirements:

##### time set to update via ntp server using:
* ntp

##### auto ban enabled for repeated SSH fails using:
* fail2ban
* note: currently set to 3 fails and 5 min ban

##### packages update automatically via cron at 4am using:
* cron-apt

##### remote monitoring of the server and multiple services using:
* nagios
* url: [http://52.26.132.12/nagios/](http://52.26.132.12/nagios/)
* username = nagiosadmin
* password = project5
* note on nagios: ssh monitoring is not set up fully.