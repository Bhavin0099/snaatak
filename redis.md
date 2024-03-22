| Author | Created on | Version | Last updated by | Last edited on |
| ------ | ---------- | ------- | --------------- | -------------- |
| Bhavin    | 21-03-24   | version 1 | Bhavin         | 21-03-24       |

# Installation of Redis
### Today we will see how to install Redis, but before installing Redis let me introduce Redis to you.

# Introduce
Redis is an open-source, in-memory data structure store that can be used as a database, cache, and message broker. It supports various data structures such as strings, hashes, lists, sets, and sorted sets, and provides high-performance, distributed, and scalable data storage and retrieval capabilities. Redis is commonly used in web applications for caching, real-time analytics, job queue management, and other use cases where fast data access is critical.

Now times, Redis is a best option for modern database, that you can use for your next application. One of the best thing which is gives by redis is low latency - Let's assume you have one application where alot user comes or if you have an application where you don't want downtimes to user, there you can use Redis.

## Now let's install Redis on Linux.
### There is two way to install Redis.
1. To install using apt command
2. To install using snap command

-
1. using apt

       curl -fsSL https://packages.redis.io/gpg | sudo gpg --dearmor -o /usr/share/keyrings/redis-archive-keyring.gpg
       echo "deb [signed-by=/usr/share/keyrings/redis-archive-keyring.gpg] https://packages.redis.io/deb $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/redis.list

![Screenshot from 2024-03-21 20-54-22](https://github.com/Bhavin0099/snaatak/assets/153531232/887b5f0f-367c-4983-b8bb-578a00eb818b)

       sudo apt-get update

![Screenshot from 2024-03-21 20-55-32](https://github.com/Bhavin0099/snaatak/assets/153531232/9c38408d-1fb0-4a13-a95e-0f7df3d9cca2)

       sudo apt-get install redis

![Screenshot from 2024-03-21 20-55-57](https://github.com/Bhavin0099/snaatak/assets/153531232/65d3fd95-bde6-448e-8abc-500924c55d52)

Make sure you have to write " Y / y " to install Redis.

![Screenshot from 2024-03-21 20-56-32](https://github.com/Bhavin0099/snaatak/assets/153531232/989b7577-3915-4aff-9b72-e9a832419e14)

After installing Redis using apt package you can check redis is properly runnig or not using this command.

       redis-cli ping

![Screenshot from 2024-03-22 15-14-35](https://github.com/Bhavin0099/snaatak/assets/153531232/a1350acd-b2f4-4cea-ab5d-f08a17f27082)

Ping -> ping, If Redis is running, it will return "PONG". If it's not running, you'll get an error message.


### After using this command you will install Redis on you system, But if you are lazy and don't want to write this all commands then you can use another way...

2. Using snap

Before using snap command, If snap in not installed in your system, you can you this command to install snapd in you system.

       sudo apt install snapd

After suscessfully install snapd packge in your system, now you can use snap command to install redis in one-line command.

       sudo snap install redis
       
![Screenshot from 2024-03-22 15-03-18](https://github.com/Bhavin0099/snaatak/assets/153531232/6578c2f6-2f1a-4250-af51-b872ede1e5a1)

The Snap is a command which is used to interact with the Snap system. It allows users to search for, install, update, and manage snaps on their system. Let me explain you more, The Snap is a software packaging and deployment system developed by Canonical, the company behind Ubuntu. It allows developers to package their applications and all their dependencies into a single, self-contained package called a "snap". These snaps can then be easily installed and managed on a wide range of Linux distributions that support the Snap system.

After installing Redis using snapd you can check redis is properly runnig or not using this command.
   
    redis.cli ping

Check the Redis logs to see if there are any errors or warnings. The default location for Redis logs is /var/log/redis/redis-server.log. You can view the last few lines of the log file using the tail command:

     sudo tail -f /var/log/redis/redis-server.log

In addition in these methods, if you want to remove redis, you can use this command:

      sudo apt-get purge –auto-remove redis-server

# Contact Information

| Name    | Email address                 |
|---------|-------------------------------|
| Bhavin  | bhavin.panchal.snaatak@mygurukulam.co   |

# Reference Links
- [Install Redis](https://redis.io/docs/install/install-redis/install-redis-on-linux/)
- [How to check if Redis is running?](https://www.dragonflydb.io/faq/how-to-check-if-redis-is-running)

Output:

![Screenshot from 2024-03-22 15-11-31](https://github.com/Bhavin0099/snaatak/assets/153531232/6bdf79db-4638-4ae3-ba0b-0fcb945e7687)

Ping -> ping, If Redis is running, it will return "PONG". If it's not running, you'll get an error message.

