此儲存庫包含 gRPC Node.js 中間件：攔截器、實用程式等。
＃＃＃ 介紹
這是一個實現MMOG架構和模組化編程的後端中間件。 MMOG 代表大型多人線上遊戲，許多玩家同時登入並玩遊戲。 在這種情況下，我的目標是設計一個在網路遊戲中經常存在的通用系統和通用功能。 我將它們抽象化為中間件，以供將來維護和新的特定遊戲設計。


MMOG 的伺服器可能包括「GameServer」、「WorldServer」、「AuthServer」、「MessageServer」、「LoginServer」、「DatabaseServer」、「CommonDatabaseServer」、「ProxyServer」和「LogServer」。 其中，「GameServer」附加有「WorldServer」、「DatabaseServer」、「ProxyServer」等。並且根據玩家群的規模可以有很多。 有一個附加到“DatabaseServer”和“CommonDatabaseServer”的“DBMS”。

  
使用案例：整體典型MMOG伺服器架構設計如下。 這裡同時使用了空間分割法和平行世界法。 空間劃分方法是指將整個世界地圖劃分為小區域，每個集群/進程（GameServer）為每個區域服務。 平行世界方法建立了一個新的整個世界，其中資料庫系統和遊戲伺服器與另一個世界分開。

圖片來源：本內容參考了 Kengo Nakajima 的《オンラインゲームを支える技術 -- 積木なプurei空間の舞台裡》。

  
在這種架構中，線路表示一台伺服器與另一台承載不同角色和功能的伺服器之間的通訊。 這種通訊可以是單向的或雙向的。 我尋求遠端過程呼叫框架 - gRPC 作為重要的技術堆疊之一。 由於其效率，我們可以設計一個低延遲且有狀態的大型多人線上遊戲伺服器系統。

### 客戶端支援
在本例中，Godot 引擎是客戶端的唯一支持，使用 Websocket Secure 進行伺服器-客戶端通訊。




