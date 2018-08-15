# guacamole-compose
### A simple way to create a guacamole server using docker compose

### To get started
Make sure you have docker and docker-compose installed: 

*  Docker: https://docs.docker.com/install/

*  Docker-compose: https://docs.docker.com/compose/install/

Once Docker and Docker-compose are installed run: 

*  docker run --rm guacamole/guacamole /opt/guacamole/bin/initdb.sh --mysql > initdb.sql

This generates the .sql script needed to initiate the database for guacamole to use

Now we are almost ready to start the server, before you do - you will need to change the variables in .env to what works for you

Once that is set go ahead and run:

* docker-compose up -d

Now docker will go ahead and pull the images, and build the containers. Once the containers are up and running it will take about 5 minutes for the database to setup before you can go to http://ServerIP:8080/guacamole

Once it's all setup you can now login, the username/password is guacadmin (I would highly reccomend changing that once signed in)


Thats all! For additional refrences on how to administrate a guacamole server visit https://guacamole.apache.org/doc/gug/
