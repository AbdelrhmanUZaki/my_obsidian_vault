---
share_link: https://share.note.sx/b9xytxr2#zRBRVAR67Op/KKA26BQW8E04t7zllHbkuLNcvsqSWtw
share_updated: 2023-12-02T22:33:09+02:00
dg-publish: true
---
  

### Network Layer Characteristics:

  

`The Network` **`Layer:`**

Provides services to allow end devices to exchange data.  
  
- ( IPv4 ) and ( IPv6 ) are the principal network layer communication protocols.

  

The network layer performs ==four== basic operations:  

1. Addressing end devices:  
بيحط IP ال source و IP ال destination  

2. Encapsulation:  
from Transport to Network layer —> بتعمل ==باكت== —> doing Encapsulation by adding IP header and it becomes packet  

3. Routing:  
بيوصل ال sender بال receiver  

4. De-encapsulation:  

![[/Untitled 17.png|Untitled 17.png]]

---

`IP Encapsulation:`

- IP encapsulates the transport layer segment
    
    ![[/Untitled 1 6.png|Untitled 1 6.png]]
    

---

`Characteristics of` `IP``:`

- ==Connectionless==:  
    - ال IP مبيعملش connection مع الوجهة قبل ما يبعت ال packet  
    - There is no control information needed ( synchronizations, acknowledgments, …..)  
    - المُستقبِل مبيبقاش عارف مسبقا إن في رسالة هتتبعت له  
    - If there is a need for connection-oriented traffic, then another protocol will handle this (typically TCP at the transport layer).
- ==Best Effort==:  
    - ال IP مش بيضمن وصول الرسالة ومش مسؤول عنها ولا مسؤول أنه يبعتها تاني  
    - مفيش acknowledgments
- ==Media Independent:  
    ==- IP ملوش علاقة أنت استخدمت أي نوع سلك.  
    - ميقدرش يتحكم في الPackets اللي بتتبعت ولا يقدر يصلح اللي باظت  
    - ميقدرش يرتب ال Packets بعد ما توصل  
    - _ال IP بيعتمد على Other protocols عشان تعمل الوظايف دي  
    _- IPv6 does not fragment packets.

---

`IPv4 Packet:`

- In binary
- diagram is read form left to right, 4 bytes per line
- The two most important fields are the source and destination
- مهم الجدول
    
    ![[/Untitled 2 7.png|Untitled 2 7.png]]
    
    ![[/Untitled 3 5.png|Untitled 3 5.png]]
    

---

`IPv6 Packets:`

- عملت تطور كبير على الـ IPv4
    
    ![[/Untitled 4 5.png|Untitled 4 5.png]]
    
- Simplified NOT smaller
    
    ![[/Untitled 5 5.png|Untitled 5 5.png]]
    
- Video at 18:00
    
    ![[/Untitled 6 3.png|Untitled 6 3.png]]
    

---

`How a Host Routes:`

  
[ Host Forwarding Decision ]

- Packets are always created at the source.
- Each host devices creates their own routing table.
- A host can send packets to the following:  
    - Itself –—> 127.0.0.1 (IPv4), ::1 (IPv6)  
    - Local Hosts – destination ==MAC Address== is on the same LAN  
    - Remote Hosts.
- لما تيجي تبعت رسالة لحد برة ال LAN فهيكون ال Router بتاعتك is the default Gateway

---

`Introduction to Routing:`

- Default Route —> لو جالك حد متعرفهوش أو متعرفش توديه فين
    
    ![[/Untitled 7 3.png|Untitled 7 3.png]]
    
      
    
- 3 Types of Router Routing Table
    - 1. Directly Connected.  
        زي الجدول اللي في الصورة اللي فوق دي  
        2. Remote (==Manually -static route-== | ==Dynamic== ).  
        لو عايز تبعت رسالة لجهاز مش في نفس ال LAN بتاعتك  
        3. Default Route.  
        لو جالك حد متعرفهوش أو متعرفش توديه فين