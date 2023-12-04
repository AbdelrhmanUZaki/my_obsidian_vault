---
share_link: https://share.note.sx/6vz03fby#sP0fAoZDZ/gkrqLErVfsYci5VGWdF6/msuJrrk3F08I
share_updated: 2023-12-02T21:58:26+02:00
dg-publish: true
---
  

`Objective`:

Role of protocols and standard organizations it facilitating interoperability in network communications

  

## Part 1

  

`**Protocol**`:

Rules describe what steps will be done to send a message from place to another.

### Resources:

  

[https://www.youtube.com/watch?v=ExVfWLsJGJQ&list=PLPBnj6azlABanyaILYOT0FKKtcSoeOc2A&index=4](https://www.youtube.com/watch?v=ExVfWLsJGJQ&list=PLPBnj6azlABanyaILYOT0FKKtcSoeOc2A&index=4)

==**Module 3 : Protocols and Models Part**== ==1==

[https://www.youtube.com/watch?v=U1-LpzDtm7g&list=PLPBnj6azlABanyaILYOT0FKKtcSoeOc2A&index=5](https://www.youtube.com/watch?v=U1-LpzDtm7g&list=PLPBnj6azlABanyaILYOT0FKKtcSoeOc2A&index=5)

==**Module 3 : Protocols and Models Part 2**==

  

  

  

`**Models**`:

Describe what are these steps and describe their exact functions.

---

`Communications Fundamentals`:

- Source ( sender )
- Destination ( receiver )
- Channel ( media ) الوسيط اللي بينقل الرسالة من المُرسِل للمستقبل

---

`Communications Protocols`:

- All communications are governed by protocols.
- Protocols are the rules.
- Rules will vary depending on the protocol

---

`Rule Establishment`:

- An identified ==sender== and ==receiver==.
- Common ==language== and ==grammar==.
- Speed and ==timing== of delivery.
- ==Confirmation== or acknowledgment requirements.

---

`Network Protocol Requirements`:

Common computer protocols must be in agreement and include the following requirements:

1- Message ==encoding.==

- process of converting information into another acceptable form for transmission.
- ==Note That: Decoding reverses this process to interpret the information.==

2- Message ==Formatting and Encapsulation.==

- Message must use a specific format.  
    الرسالة لازم تكون بمواصفات/ شكل معين عشان ينفع تتبعت
- Message Formats depend on the type of message and the channel.

3- Message ==Size.==

عشان تبعت رسالة كبيرة لازم تتقسم لأجزاء صغيرة بعدين ترجع تتجمع تاني عند المُستقبِل  
عشان لو حصل مشكلة وأنت كنت باعت الملف كله مرة واحدة، هيضيع الملف كله كدا

4- Message ==T====iming.==

- Flow Control:
    
    كل جزء من الداتا اتبعت أد اي وسرعته أد اي واتبعت امتى ووصل امتى
    
- Response Timeout:
    
    Manages how long a device waits when it does not hear a reply from the destination.
    
- Access method:
    
    Determines when someone can send a message.
    

5- Message ==Delivery Options.==

- Unicast
    
    One to one communication.
    
- Multicast
    
    One to many.
    
- Broadcast
    
    One to all.
    

![[/Untitled 13.png|Untitled 13.png]]

Message Delivery Options.

---

  

`Network Protocol Overview`:

- Network protocols define a common set of rules.  
    
- Can be implemented on devices in:  
    - Software  
    - Hardware  
    - Both
- Protocols have their own:  
    - Function  
    - Format  
    - Rules

  

`Some Of Protocol Types`

|==Protocol Type==|==Description==|
|---|---|
|Network Communications|Enable two or more devices to communicate over one or more networks.|
|Network Security|Secure data to provide authentication, data integrity, and data encryption.|
|Routing|Enable routers to exchange route information, compare path information, and select best path.|
|Service Discovery|Used for the automatic detection of devices or services.|

---

  

`Network Protocol Functions`:

|==Function==|==Description==|
|---|---|
|Addressing|Identifies sender & receiver|
|Reliability|Provides guaranteed delivery \| بيأكد أن تم وصول البيانات للشخص الثاني|
|Flow Control|Ensures data flows at an efficient rate|
|Sequencing|Uniquely labels each transmitted segment of data|
|Error Detection|Determines if data became corrupted during transmission|
|Application Interface|Process-to-process communications between network applications|

---

  

`Protocol Interaction`:

|==Protocol==|==Function==|
|---|---|
|Hypertext Transfer Protocol (HTTP)|1- Governs the way a web server and a web client interact  <br>2- Defines content and format.|
|Transmission Control Protocol (TCP)|1- Manages the individual conversations.  <br>2- Provides guaranteed delivery.  <br>3- Manages flow control.|
|Internet Protocol (IP)|Delivers messages globally from the sender to the receiver|
|Ethernet|Delivers messages from one NIC to another NIC on the same Ethernet Local Area Network (LAN)|

---

  

`Network Protocol Suite`:

  

Layers Name:

1- Application

2- Transport

3- Internet

4- Network

في كل مربع ملون، أنت بتختار حاجة واحدة بس.

![[/Untitled 1 4.png|Untitled 1 4.png]]

---

Protocol Stack = Protocol Suite

  

![[/Untitled 2 5.png|Untitled 2 5.png]]

---

---

  

```
## More Details:
```

  

![[/Untitled 3 3.png|Untitled 3 3.png]]

|   |   |
|---|---|
|Transport layer ( TCP )|- Connection-Oriented  <br>- المستقبل بيديك تأكيد إن الحاجة وصلت|
|Transport layer ( UDP )|- Connectionless  <br>- المستقبل مش بيديك تأكيد إن الحاجة وصلت  <br>- Ex: المكالمات|
|Application Layer ( FTP )|sending \| receiving files.|

---

  

### الخطوات اللي بتحصل عشان تبعت أو تستقبل رسالة

![[/Untitled 4 3.png|Untitled 4 3.png]]

---

  

### The benefits of using a layered model

  

OSI & TCP/IP Models

![[/Untitled 5 3.png|Untitled 5 3.png]]

---

## Part 2

  

![[/Untitled 6 2.png|Untitled 6 2.png]]

---

  

`Benefits of Using a layered Model`:

- الدنيا بتبقى منظمة أكتر، فلو حصل مشكلة بتروح تدور في ==طبقة== معينة مش كل الشبكة كلها.
- بيعمل منافسة بين المصنعين عشان يجيبوا أحسن ما عندهم.
- لو حصل تغير في layer معينة دا مش هيأثر على الـ layers التانية
- provide a common language to describe networking functions and capabilities. | بيسهل عليك أنت الدنيا كدا يعني عن طريق أنه بيظبطلك شوية خطوات كدا عشان اي الـ functions بتاعت كل واحدة فيهم ويعرفك إمكانيات واحدة فيهم

  

`مهمة، لازم تكون حافظها`

![[/Untitled 7 2.png|Untitled 7 2.png]]

- 7- ==Application==:  
    Protocols you use but before doing anything ex: HTTP, FTP.
- 6- ==Presentation==:  
    بيديك شكل للداتا قبل ما تبعتها
- 5- ==Session==:
    
    كأنك فاتح سيشن بداية من أنك بتبعت الرسالة لحد ما تخلص  
    لازم تكون مفتوحة في وقت معين، توصل الرسالة، وتاخد acknowledgement  
    لو الرسالة وصلت ومرجعش لك acknowledgement هتقوم السيشن مقفولة
    
- 4- Transport:  
    مسؤولة عن نقل الداتا بالـ 2 بروتوكول، TCP, UDP
- 3- Network:  
    بيتحكم في ال ipهات بتاعتك  
    أنت هتشتغل على ip version 4 ولا version 6  
    - مش بيشتغل إلا على الراوتر
- 2- Data Link:  
    هي اللي بتشتغل على السويتش،
- 1- Physical:  
    السلك نفسه بقى، الداتا هتمشي عليه ازاي

|   |   |   |
|---|---|---|
|Data link ( Layer 2 )  <br>Switch|بيشتغل على ال Mac address.  <br>- fixed for one device.  <br>- NIC دا اللي جواه ال Mac address بتاعي.  <br>- Mac address is unique.|We use mac addresses to send messages in our LAN network|
|Network ( Layer 3 )  <br>router|بيشتغل على ال virtual ip  <br>- IP here changes every time you entered the internet, but it is still unique.|We use IPs to send messages to devices in another LAN network or in any place in world|

  

==**IP —> Logical address**==

==**Mac address —> Physical address**==

---

  

`Data Encapsulation`:

  

- $\text{Segmenting Messages}:$﻿  
    - ==Segmenting==:  
    breaking up messages into smaller units.  
    - ==Multiplexing==:  
    taking multiple streams of segmented data and interleaving them together  
    - ==Benefits of Segmenting Messages==:

- increases speed.

- increases efficiency:  
Only segments that fail to reach the destination need to be retransmitted, not the entire data stream.

  

- $\text {Sequencing}:$﻿  
    ترقيم الأجزاء اللي اتقطعت دي عشان لما توصل تتجمع تاني بالترتيب المظبوط بتاعها

  

- $\text {Protocol Data Units (PDU)}:$﻿  
    1. Data (Data Stream)
    2. Segment
    3. Packet
    4. Frame
    5. Bits (Bit Stream)
        
        كل حتة داتا اتقطعت Segment هيُطبق عليها الخطوات دي
        

- $\text {De-encapsulation:}$﻿ عكس الخطوات
    1. Received as Bits (Bit Stream)
    2. Frame
    3. Packet
    4. Segment
    5. Data (Data Stream)

---

  

`Data Access`:

- Comparison between Network and Data link layers ( [[Protocols and Models ( Module 3 )]] )

  

- Layer 3 Logical Address (IP):  
    The IP packet contains TWO IP addresses:  
    • Source IP address  
    • Destination IP address

  

- An IP address contains two parts:
    
      
    1. Network portion (IPv4) or Prefix (IPv6)
    
    • The left-most part of the address indicates  
    the network group which the IP address is  
    a member.  
    • Ech LAN or WAN will have the same  
    network portion.
    
    2. Host portion (IPv4) or Interface ID (IPv6)
    
    • The remaining part of the address identifies  
    a specific device within the group.  
    • This portion is unique for each device on  
    the network.
    

  

- $\text {Sending Message over WAN network:}$﻿  
    جامدة جدا، مشروحة في الفيديو كويس لو مش فاهم هنا  
    بس الفكرة عامة يعني  
    أن ال source و ال destination بتوع ال Data Link layer بيتغيروا  
    مع كل خطوة \ محطة، ال destination بتبقى هي المحطة الجديدة، وال Source بيكون هو المحطة اللي كانت destination -old one-  
    بس طبعا ال source, destination اللي في ال Network Layer لازم يكونوا ثابتين ميتغيروش، عشان ال Destination تعرف الرسالة اللي جت لها دي جاية منين  
    وممكن عشان كمان لو هي بتستخدم TCP protocol فهيكون في رد تأكيد على وصول الرسالة فلازم بقى يكون عندك/ تكون عارف ال source الأصلي
    
    ![[/Untitled 8 2.png|Untitled 8 2.png]]
    
    ![[/Untitled 9 2.png|Untitled 9 2.png]]
    
    ![[/Untitled 10 2.png|Untitled 10 2.png]]
    
    ![[/Untitled 11 2.png|Untitled 11 2.png]]
    
    ![[/Untitled 12 2.png|Untitled 12 2.png]]
    
    ![[/Untitled 13 2.png|Untitled 13 2.png]]
    
    ![[Untitled 14.png]]
    
    ![[Untitled 15.png]]