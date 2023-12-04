---
share_link: https://share.note.sx/1cph26pb#Kz5e9CvNmj8DL8ezIzOf7O3n2GgV9jcItA6BqtutHmo
share_updated: 2023-12-02T22:33:05+02:00
dg-publish: true
---
  

### Purpose Of Data Link Layer:

  

`The data link layer:`

- It allows upper layer -Network layer- protocols to access the physical layer media.
- Performs error detection and rejects corrupts frames
- Encapsulates Layer 3 packets (IPv4 and IPv6) into Layer 2 Frames.
- مسؤولة أنها توصل الأجهزة ببعض  
    عن طريق ال Network Interface Cards (**==NIC==**)

  

$\text {Data link layer} =~ \begin{cases}\text{Logical Link Control \small Cublayer \color{Red}(LLC)} \\$

  

1. ==MAC== sublayer:
    
    Is responsible for data encapsulation and media access control.
    
    - encapsulation: means يضيف ال MAC Adress بتاع ال source ,destination
    - هو اللي هيبعت الداتا عشان تمشي على الميديا بتاعتي
    

1. ==LLC== sublayer:
    
    Communicates between the networking ==software== at the upper layers and the device hardware at the lower layers.
    

---

  

`Providing access to media:`

![[/Untitled 16.png|Untitled 16.png]]

---

  

### Topologies:

Is the arrangement and relationship of the network devices and the interconnections between them.

Two Types :

1. Physical topology:  
    physical connections and how devices are interconnected.
2. Logical topology:  
    virtual connections between devices using device interface and IP addressing schemes.

`WAN Topologies:`

3 Types

1. ==Point-to-point==: Permanent link between two endpoints via Network between them.
2. ==Hub and spoke==  
    
    ![[/Untitled 1 5.png|Untitled 1 5.png]]
    
3. ==Mesh  
    ==كل جهاز متوصل بكل الأجهزة

`LAN Topologies:`

1. ==Bus==
2. ==Ring==
3. ==Star==
4. ==Extended Star==
5. ==Mesh==

---

  

`Half and Full Duplex Communication:`

- Half-duplex —> الجهاز الواحد إما هيستقبل أو هيبعت
- Full-duplex —> الجهاز الواحد ممكن يستقبل ويبعت في نفس الوقت

  

`Access Control Methods:`

- CSMA/CD —> Wired  
    CSMA/CA —> Wireless  
    
    ![[/Untitled 2 6.png|Untitled 2 6.png]]
    
    Deterministic access where each node has its own time to send or receive*
    

  

### **Comparison between CSMA/CD & CSMA/CA**

![[/Untitled 3 4.png|Untitled 3 4.png]]

![[/Untitled 4 4.png|Untitled 4 4.png]]

---

### Data Link Frame:  

`Frame Fields:`

Data is encapsulated by the data link layer with a header and a trailer to form a frame.

A data link frame has three parts:  
• Header  
• Data  
• Trailer

  

![[/Untitled 5 4.png|Untitled 5 4.png]]

  

---

---