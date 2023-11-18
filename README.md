## Node.js gRPC-based communication middleware for MMOGs  
This repository hold gRPC node.js middleware: interceptors, utilities, and more.
### Introduction
This is a backend middleware to achieve MMOGs architectural and modular programming. MMOG stands for the massively multiplayer online game where a lot of players log in and play concurrently at the same time. In this case, I aim to design a common system and generic functions that often exist in online games. I abstract them as middleware for future maintenance and new specific game design.  


MMOGs' servers include `GameServer`, `WorldServer`, `AuthServer`, `MessageServer`, `LoginServer`, `DababaseServer`, `CommonDatabaseServer`, `ProxyServer` and `LogServer`. Thereof, `GameServer` is attached by `WorldServer`, `DatabaseServer`, `ProxyServer`, etc. And could have many depending on the scale of the player base. There is a `DBMS` attached to `DatabaseServer` and `CommonDatabaseServer`.  

  
Use Case: The overall typical MMOG server architecture design is as follows. This uses both space division method and parallel world method. Space division method means to divide the whole world map into small region, each cluster/process(GameServer) serves each region. Parallel world method establish a new entire world for more upcoming player.
![nodejs-grpc-middleware-mmog-server-overall-architecture](https://github.com/cloudchentrial/nodejs-gRPC-middleware-mmog-server/assets/31240078/1967d792-c519-41ad-93b3-6a4f959bedf8)  
Credit: This content takes reference to オンラインゲームを支える技術 -- 壮大なプレイ空間の舞台裏 by Kengo Nakajima.  

  
In this architecture, the line indicate the communication between one server to another which carry different role and functions. This communication could be either unary or bidirectional. I seek remote procedural call framework - gRPC as one of the important technical stack. Due to its efficency, we can design a low latency and stateful massively mulitplayer online game server system.




