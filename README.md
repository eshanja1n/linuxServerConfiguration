I am having problems with connecting to my server via ssh. I would
very much appreciate it if you could take a look at the steps I went 
through and help me fix this error so I can complete this project.

I have completed all the requirements, however I simply cannot ssh to the 
server from a remote computer. When I go to the url, I am prompted with a 
screen, which I included as a screenshot in my submission, that says the apache server 
is working. 

**IP Address:** 54.213.161.244
**URL** http://54.213.161.244/

**Accessible SSH port:** 2200


-----BEGIN RSA PRIVATE KEY-----
Proc-Type: 4,ENCRYPTED
DEK-Info: AES-128-CBC,CB847CEEA6E51ED71012BAA85990434D

HBffmcBpMs2hGwh/iRQIp86D8/5d5m2ml1/jcWpTPpniVPMcA2AP19e0U5p5gTfQ
BUzKwmo5AtZEdJMoZJGxqNYavyZ/mrZskaZeiKF78g2kCypm8gcPq6rPc2TNQ1Lx
Boeysn4ZBpQEkz4R2R5GSl+dYTC4NggObeL7SYrMjPNRX/vn+NduqqF8cX8DOUuJ
hibjjAv3zEx2+Fv9j8lvNkESvZbfwcjdQ9u3NYlOx/hIEP+2liiLfZMCXLBBumjy
qt6QTeJsMAZIxEMg5m8XhMpmhciIsWWr10rHu7DrzWZkBheykEoaHrxi/QRjcd3H
pNGq9Yce/crp3vsSKZGo+kwCi5piOACNtU57Gt23nC/iWGVRmVaMypg6kHxlNbmM
TARvySGe8rWIdLZwBwkjCg7vmkyC6uTaXnqlw/6+dYJ48ieLFk2asgj1nUiwACGe
5DtIQcZy4MEi7Rfuf1Us8pEyr1u1qvy2ahygJvxCJCd8dfK5dtZ/xjWt08X1dKzY
Idm219Km98U10r2K1mHmJVp32LFUiudu9+XjJXJ762umj4twwSdQjcoALyTb0zG7
P21MemNJep63cwEUSLbqU2fvXoFFYACyHVZZBMnY12fyBZ+lEI53//ZLEoZQ6dZh
5vLncGABwAbORFPTUhWhHR6eM3kkUZlA4K31TsnCGUzH4H5CWkgImcC2HCGujQPJ
RFcJh5By6vHDkCtSLvCqgMhP1ZsLEAA2ny4tt/uH1BFfldkxPeGenZb1zu89Cgxe
zar6CeMJqBmN7xePT3TvJyKHPHtfi8ADh4zCG6QkmwqBvxxRfmWKZT51xrP1RR0w
JwNU2o6+zP7QF7FoXkNiSRkvzNfNOigDWCk55wrEhCUiRW3Yrm58Q+Od39I+uqXL
UwbUX+Sq+EPn2CTp6+UMBodKP8Rb40IbanTI7xmJXi3rfXJeDgQcAAzPQuDGF172
mb0NkHQlj01KdHGaq/AaBc2MrXHeXoyHwtKqRYhMr9Rd3hRrbKqcO73b2Wg8RLfq
E0m8iSb9h8f3NRDjhICpxj5xXw5Xkr3e+SGjD4TBfvy4zr15oQBy3cNLH/6lnquI
zjpBHtk6DjP8lwRHcxY7jPUyon4iY//sluyuZ7f+kWCi827bTt68jglmGhGmO5yI
LvWQqag4zOz7ESobmjz65jUklVCiAbRM3QWLMFcTXM6matGFyLAveqmYOxDH6Op+
eIWWn8HbJ5skdPm86kspWyeIkUeZAjDlUic2cPTmY1A7N9zA5NkAkuZQdA4bK47Y
5nKux4OWK375gHbDoAzKDdgBqmLW2P4ycrsOdI+udpKTOH579G0sBmU0im2G7C86
n5oThBknZ70lP6AzsYl8sMLL9jC8CUGgmWipi166cZBf8FFrd0cyhutcxGkDcVO8
XjCXmu7vrmCQt5xTvcH9vy4jiLNf0bMnvAlj/Pa8l4+qhjI7+fNdmOPz3Oji1y9m
rCEudnNc+mjMCi2jhq6fv9QInJ12BUBryPmwnP3I+8wM43MjiUMQ88jRxp/lxL6F
vEwqVA63YPZ0FvH/ge1FhOUJPezXQ/xqqqZXo/R95V3uw9HZ8Fx+NNV9DDFTCsMF
-----END RSA PRIVATE KEY-----


ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCzWdSFniVXsmdO89+2JE9kbSdH1930QXJB+tYaaFRkNVl2ghOHW2tp5UIjwDf49Wqr2YOQihulpIM7ocQdpdIHNgXtGwx7tlRHeGie6jcI93TZAHuGzMMBX9PIehOJUIwabMm+evnHGig8BJdRtllFfqXE04Biqnq61Mx3/mSwZIftWC5Rqbm7yY3l2Fwe/yFi+WDy4hi7S+inhvs1EP9QdZ4thMD7Fbs6IB1x2eIM3FLQmpY9xR6RsoY21JNyxUzxC9HkuFHLifw7LwkHRONT0H8nx8whZ7B/SC7uFhmleERtKtehIV9ViWv3xGW6Hl5LD3pGi6RfzlEBs0ozxTVN eshanjain@Eshans-MacBook-Pro.local


Here is the list of steps I went through. Would really appreciate it if you
can help me debug this error.:

1. created a new instance on amazon lightsail
2. clicked orange button to ssh into project. 
3. updated the installed packages
$ sudo apt-get update
$ sudo apt-get upgrade
4. Configured the Uncomplicated Firewall (UFW):
$ sudo ufw default deny incoming
$ sudo ufw default allow outgoing
$ sudo ufw allow www
$ sudo ufw allow ntp
$ sudo ufw allow 2200/tcp
$ sudo ufw enable

5. Changed the SSH port from 22 to 2200
$ sudo vim /etc/ssh/sshd_config 
#changed the port from 22 to 2200 within the file
#the restarted ssh service using:
$ sudo service ssh restart

6. added new grader user:
$ sudo adduser grader
#set password to grader
#gave `Sudo` Access to grader and set NOPASSWD
$ sudo vim /etc/sudoers.d/grader
#Edit and following line to this file
grader ALL=(ALL) NOPASSWD:ALL
#Generated a keypair and push it to server.
# on local machine, generated a key pair:
$ssh-keygen -t rsa
#copied and pasted the key from local machine, usign vim editor:
$ vim .ssh/authorized_keys
#Changed permission of `.ssh` and `.ssh/authorized_keys`
$ chmod 700 .ssh
$ chmod 644 .ssh/authorized_keys

7. Changed timezone to UTC:
$ sudo timedatectl set-timezone UTC

8. Install and configure Apache to serve a Python mod_wsgi application.
$ sudo apt-get install apache2 libapache2-mod-wsgi
**Enabled mod_wsgi:**
$ sudo a2enmod wsgi

9. Installed and configured PostgreSQL:
$ sudo apt-get install libpq-dev python-dev
$ sudo apt-get install postgresql postgresql-contrib

10. Created new database user named **catalog** 
$ sudo su - postgres
$ psql

* Create a new database named *catalog*:    `# CREATE DATABASE catalog;`
* Create a new user named *catalog*:    `# CREATE USER catalog;`
* Set a password for catalog user:    `#  ALTER ROLE catalog with password 'password';`
* Grant permission to catalog user:    `# GRANT ALL PRIVILEGES ON DATABASE catalog TO catalog;`
* Exit from psql:    `# \q;`
* Return to grader using: `$ exit`

11. Installed python-pip, Flask and other dependencies.
`$ sudo apt-get install python-pip
$ sudo pip install Flask
$ sudo pip install sqlalchemy psycopg2 sqlalchemy_utils
$ sudo pip install httplib2 oauth2client requests

12. Changed the database connection to:
engine = create_engine('postgresql://catalog:password@localhost/catalog')

13. clone my git repo into project:
$ sudo mkdir /var/www/ItemCatalogFlaskApp
$ sudo mkdir /var/www/ItemCatalogFlaskApp/FlaskApp

* Made `grader` as ownner of that directory
$ sudo chown -R grader:grader /var/www/ItemCatalogFlaskApp
#cloned repo into /var/www/ItemCatalogFlaskApp/FlaskApp
$ sudo git clone https://github.com/eshanja1n/itemcatalog

14. Create the .wsgi file in *ItemCatalogFlaskApp*:
$ cd /var/www/ItemCatalogFlaskApp/
$ sudo vim ItemCatalogFlaskApp.wsgi
* Added the following lines of code to the `.wsgi file`
```python
#!/usr/bin/python
import sys
import logging
logging.basicConfig(stream=sys.stderr)
sys.path.insert(0,"/var/www/ItemCatalogFlaskApp")
from FlaskApp import app as application
```
15. Configuref and Enabled New Virtual Host:
$  sudo vim /etc/apache2/sites-available/000-default.conf
#added the following lines to the file
```xml
<VirtualHost *:80>
    ServerName 'test1'
    ServerAdmin nishmaj@gmail.com
    WSGIScriptAlias / /var/www/ItemCatalogFlaskApp/ItemCatalogFlaskApp.wsgi
    <Directory /var/www/ItemCatalogFlaskApp/FlaskApp>
        Order allow,deny
        Allow from all
    </Directory>
    Alias /static /var/www/ItemCatalogFlaskApp/FlaskApp/static
    <Directory /var/www/ItemCatalogFlaskApp/FlaskApp/static/>
        Order allow,deny
        Allow from all
    </Directory>
    ErrorLog /home/grader/serverErrors/serverError.log
    LogLevel warn
    CustomLog /home/grader/serverErrors/access.log combined
</VirtualHost>
```

16. enabled virtual host:
$ sudo a2ensite 000-default

17. 7. Restarted Apache to run the app on sever:
$ sudo apt-get purge apache2
$ sudo apt-get install apache2


#Whenever I try to ssh to the server from my terminal or another computer, 
#I am never able to connect. I included a screenshot of the error I recieve
#when I try to do this. 
