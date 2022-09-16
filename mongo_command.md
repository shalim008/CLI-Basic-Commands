
# Mongo DB

### Basic

      $ docker pull mongo
      $ docker run -d -p 27017:27017 --name database_name mongo    // run database service
      $ docker ps   // check docker status
      $ docker logs -f database_name //check mongo container logs
      $ docker exec -it database_name /bin/bash  // to enter the mogo container in local environmet. 



### Install Mongo
$ docker pull mongo

### Start a mongo server instance
$ docker run -d -p 27017:27017 --name database-mongo mongo

### Container shell access and viewing MongoDB logs
The docker exec command allows you to run commands inside a Docker container. The following command line will give you a bash shell inside your mongo container:

$ docker exec -it some-mongo /bin/bash

The MongoDB Server log is available through Docker's container log:

$ docker logs some-mongo



1
-- Now we can open interactive terminal for mongo

$ docker exec -it shopping-mongo /bin/bash


2
-- After that, we are able to run mongo commands. 
Let me try with 

 - $ create database
 - $ create collection
 - $ add items into collection
 - $ list collection


$ ls
$ mongo
$ show dbs
$ use CatalogDb  --> for create db on mongo
$ db.createCollection('Products')  --> for create people collection

$ db.Products.insertMany([{ 'Name':'Asus Laptop','Category':'Computers', 'Summary':'Summary', 'Description':'Description', 'ImageFile':'ImageFile', 'Price':54.93 }, { 'Name':'HP Laptop','Category':'Computers', 'Summary':'Summary', 'Description':'Description', 'ImageFile':'ImageFile', 'Price':88.93 } ])


$ db.Products.find({}).pretty()
$ db.Products.remove({})

$ show databases
$ show collections
$ db.Products.find({}).pretty()
