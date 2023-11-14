## Node.js gRPC communication middleware for MMOGs
### Introduction
This repository is a backend middleware to achieve MMOGs architectural and modular programming.  
MMOGs' servers include `GameServer`, `WorldServer`, `AuthServer`, `MessageServer`, `LoginServer`, `DababaseServer`, `CommonDatabaseServer`, `ProxyServer` and `LogServer`. Thereof, `GameServer` is attached by `WorldServer`, `DatabaseServer`, `ProxyServer` and could have many depending on the playerbase. There is a `DBMS` attached to `DatabaseServer` and `CommonDatabaseServer`.  
The overall MMOGs server architecture design is as follows,  
![nodejs-grpc-middleware-mmog-server-overall-architecture](https://github.com/cloudchentrial/nodejs-gRPC-middleware-mmog-server/assets/31240078/422fd0c0-a3f0-476c-b0e7-4722cefed8b0)



