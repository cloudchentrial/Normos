## Node.js gRPC-based communication middleware for MMOGs
### Introduction
This repository is a backend middleware to achieve MMOGs architectural and modular programming. MMOG stands for the massively multiplayer online game where a lot of players log in and play concurrently at the same time. In this case, I aim to design a common system and useful functions that often exist in online games. I abstract them as middleware for future maintenance and new specific game design.
MMOGs' servers include `GameServer`, `WorldServer`, `AuthServer`, `MessageServer`, `LoginServer`, `DababaseServer`, `CommonDatabaseServer`, `ProxyServer` and `LogServer`. Thereof, `GameServer` is attached by `WorldServer`, `DatabaseServer`, `ProxyServer` and could have many depending on the playerbase. There is a `DBMS` attached to `DatabaseServer` and `CommonDatabaseServer`.  
The overall MMOGs server architecture design is as follows,  
![nodejs-grpc-middleware-mmog-server-overall-architecture](https://github.com/cloudchentrial/nodejs-gRPC-middleware-mmog-server/assets/31240078/422fd0c0-a3f0-476c-b0e7-4722cefed8b0)  
In this architecture, the line indicate the communication between one server to another which carry different role and functions. This communication could be unary or bidirectional. I seek remote procedural call framework - gRPC as one of the important technical stack. Due to its efficency, we can design a low latency and stateful massively mulitplayer online game server system using gRPC.  




