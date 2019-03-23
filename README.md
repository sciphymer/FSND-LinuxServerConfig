# FSND-Project3-LinuxServerConfig

1.Server info:
IP address: 13.228.70.143
SSH port: 2200

2.Hosted Web Application:
http://13.228.70.143.xip.io

3.Software installation:
- Python module installed inside Python virtual environment
Package        Version
-------------- --------
certifi        2019.3.9
chardet        3.0.4
Click          7.0
Flask          1.0.2
Flask-HTTPAuth 3.2.4
httplib2       0.12.1
idna           2.8
itsdangerous   1.1.0
Jinja2         2.10
MarkupSafe     1.1.1
oauth2client   4.1.3
passlib        1.7.1
pip            19.0.3
psycopg2       2.7.7
pyasn1         0.4.5
pyasn1-modules 0.2.4
requests       2.21.0
rsa            4.0
setuptools     40.8.0
six            1.12.0
SQLAlchemy     1.3.1
urllib3        1.24.1
Werkzeug       0.15.1
wheel          0.33.1
- Software installed in local:
python-pip/xenial-updates,now 8.1.1-2ubuntu0.4 all
apache2/xenial-updates,now 2.4.18-2ubuntu3.9 amd64
libapache2-mod-wsgi/xenial,now 4.3.0-1.1build1 amd64
postgresql/xenial-updates,now 9.5+173ubuntu0.2 all

- Configuration changes:
i. created user "grader", added in sudoers and added SSH key-based authentication.
ii. UFW configured to allow connections for SSH in port 2200, HTTP in port 80 and NTP in port 123.
iii. Apache2 server added site config for WSGI Flask application.
iv. Uploaded Flask WSGI application to /var/www/flaskapp.
v. PostgreSQL Database server added dbadmin user, configured it's DB access and authentication method in pg_hba.conf

- 3rd party resource referenced:
https://www.digitalocean.com/community/tutorials/how-to-create-remove-manage-tables-in-postgresql-on-a-cloud-server
https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-16-04
https://modwsgi.readthedocs.io/en/develop/index.html
http://fredericiana.com/2014/11/29/sqlite-error-open-database-file/
https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps

4. SSH Key location of 'grader' user
/home/grader/.ssh/authorized_keys
