# Linux Server Configuration

Configuration of a baseline installation of a Linux server on a virtual machine to host Python web applications. This inlcudes installing updates, securing the server from attack vectors, installing/configuring a PostgreSQL database, and user management.


## Server Details

* IP address: 18.217.71.167
* SSH Port: 2200
* URL to hosted application: http://18.217.71.167


## Software & Configurations

Summary of software installed...

* Apache
* Python 2.7
* PostgreSQL
* Git


Configurations...

* The Uncomplicated Firewall (UFW) only allows incoming connections from
	- SSH (port 2200)
	- HTTP (port 80)
	- NTP (port 123)
* Disabled remote login of root user
* Remote connections to the database are not allowed

## Additional Resources

The following articles were helpful in configuring the server.

Disable SSH logins for the root account

https://www.a2hosting.com/kb/getting-started-guide/accessing-your-account/disabling-ssh-logins-for-root

Deploying a Flask Application on an Ubuntu VPS

https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps

How To Secure PostgreSQL on an Ubuntu VPS

https://www.digitalocean.com/community/tutorials/how-to-secure-postgresql-on-an-ubuntu-vps

Stack Overflow (https://stackoverflow.com)

Various articles helped me overcome the issues I had in setting up the Python virtual environment. Many thanks to the people who kindly answer questions!


## Web Application

The server is configured to run a Python web server as a WSGI app with a PostgreSQL database. The web application is a store catalog app (https://github.com/zindigo/store-catalog), which can be viewed in the browser at http://18.217.71.167.

