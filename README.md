## Node.js gRPC communication middleware for MMOGs
### Introduction
This repository is a backend middleware to achieve MMOGs architectural and modular programming.  
MMOGs' servers include `GameServer`, `WorldServer`, `AuthServer`, `MessageServer`, `LoginServer`, `DababaseServer`, `CommonDatabaseServer`, `ProxyServer` and `LogServer`. Thereof, `GameServer` is attached by `WorldServer`, `DatabaseServer`, `ProxyServer` and could have many depends on the playerbase. There is a `DBMS` attached to `DatabaseServer` and `CommonDatabaseServer`.  
The overall design is as follows,  


