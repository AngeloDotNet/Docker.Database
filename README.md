# Docker Database
There are currently the following templates:

## Database
- SQL Server 2017 Express
- SQL Server 2019 Express
- SQL Server 2022 Express
- MySQL Server 5.7
- Postgres 9.6
- Postgres 13.1

If you like this repository, please drop a ⭐ on Github!

## Network configuration
The docker-lan network (bridge type) was created with the command: 

> docker network create --driver=bridge --subnet=192.168.100.0/24 docker-lan

### For Postgres 13.1 database (For Kong) 
It is recommended to change the USERNAME, PASSWORD and DATABASE NAME

> CREATE USER user_kong WITH PASSWORD 'pass_kong1!';
> CREATE DATABASE db_kong OWNER user_kong;

### For Postgres 9.6 database (For Konga) 
It is recommended to change the USERNAME, PASSWORD and DATABASE NAME

> CREATE USER user_konga WITH PASSWORD 'pass_konga1!';
> CREATE DATABASE db_konga OWNER user_konga;

### Important
Before starting the related Kong and Konga dockers, modify the USERNAME, PASSWORD and DATABASE NAME indicated in the relevant dockers and compose with the same data used in the commands previously used to create USER and DATABASE. 

Also change the IP-SERVER-DOCKER parameter by replacing it with the ip address of the server hosting the dockers. 

The dockers kong-migration and konga-migration, present in the docker compose of Kong and Konga, are used only for the first time to create the database structures for the corresponding services.
