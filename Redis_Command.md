# Redis Commands

    $ docker pull redis
    $ docker run -d -p 6379:6379 --name aspnet-run redis  // run container
    $ docker logs aspnet-run   // logs 
    $ docker exec -it aspnet-run /bin/bash  // interactive terminal to run redis CLI command

1
-- Now we can open interactive terminal for redis

    $ docker exec -it aspnetrun-redis /bin/bash


2
-- After that, we are able to run redis commands. 
Let me try with 

     $ redis-cli
     $ ping - PONG
     $ set key value
     $ get key
     $ set name mehmet
     $ get name
