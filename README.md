docker-apache-http-tomcat
=========================

A Dockerfile repository to create an image with an Apache HTTP Server redirecting requests to an Apache Tomcat.

Building the base image
-----------------------

To create the base image `dezoito18/apache-http-tomcat`, execute the following command on the apache-http-tomcat folder:

	docker build -t dezoito18/apache-http-tomcat .


Running your docker image
-------------------------

Start your image binding the external ports 80 in all interfaces to your container:

	docker run -d -p 80:80 -e TOMCAT_PASS="password" dezoito18/apache-http-tomcat

Test your deployment by accessing Tomcat Manager application on:

	http://localhost/manager
