---
share_link: https://share.note.sx/7ursugpx#HGJ1QTfqYXKUrfW1P7joREw8kNH4UA0lN4AdVZXHtso
share_updated: 2023-12-02T21:58:18+02:00
dg-publish: true
---
  

  

[https://youtu.be/IuL8xra_Pyk](https://youtu.be/IuL8xra_Pyk)

  

  

![[ITN_Module_14.pdf]]

---

السلايد هتكون في نفس الصفحة، وقصادها هكتب لو حاجة مش فاهم معناها أو محتاجة شرح أو ملحوظة

السلايد قد تكون مش كاملة -ممكن آخد جزء منها بس

---

  

## Role of the Transport Layer

  

![[/Untitled 21.png|Untitled 21.png]]

- كل اتصال ملوش علاقة بالتاني، حتى لو بنفس الIP ودا بيحصل فعلا لأن البيت الواحد له IP واحد ومع ذلك مفيش اتصال بيخش على التاني في البيت الواحد.
- بيوصل الداتا من كل الـ Layers اللي تحته، للطبقة اللي فوقه -Application Layer- والعكس

  

---

![[/Untitled 1 9.png|Untitled 1 9.png]]

  

- بيضيف header information على الـ Packet عشان تبقى Segment
- Multiplexing → بيعمل أكتر من حاجة في نفس الوقت

---

![[/Untitled 2 10.png|Untitled 2 10.png]]

- الاتنين (FTP , TFTP )بيستخدموا عشان ينقلوا ملفات، لكن
    - FTP → has acknowledgement
    - TFTP → hasn’t

  

---

![[/Untitled 3 8.png|Untitled 3 8.png]]

- بيرقم ويتتبع نقل الـ segments للـ host المعين في ال application المعين
- لو في Packet وقعت في نص الطريق، فمش هترجع acknownledge فيطلبها تاني من ال sender بعد شوية وقت
- بيحدد حجم الـ segment حسب الـ Receiver هيستحمل اد اي

---

![[/Untitled 4 7.png|Untitled 4 7.png]]

- UDP مش بتعوز acknowledgment
- لو Packet وقعت مش برجع أبعتها تاني
- [[Transportation of Data ( Module 14 )]]

  

---

### Comparison between UDP & TCP

![[/Untitled 5 7.png|Untitled 5 7.png]]

- UDP
    - low overhead → عشان مش بيعمل retransmit للداتا
- TCP
    - Reliable → بيتأكد من وصول كل جزء أنت بعته
    - بيرتب الـ Segments بنفس الترتيب اللي أنت بعته

  

---

### **TCP**

- TCP Features

- Establishes a Session (connection)
    - Session → زي أنبوبة كدا بين المرسل والمستقبل
- Ensures Reliable Delivery.
- Provides Same-Order Delivery.
- Supports Flow Control.

![[/Untitled 6 5.png|Untitled 6 5.png]]

---

### TCP Header Fields

![[/Untitled 7 5.png|Untitled 7 5.png]]

- Source Port → زي رقم التليفون بتاعك اللي هتبعت بيه رسالة
- Destination Port → عايز تروح لأي بروتوكول مستخدم
- Window Size → أقل حجم تقدر تبعته من المرسل للمستقبل
- Urgent → لو في Segment مهمة تتبعت، فأنت بتأكد عليه أنها لازم تتبعت دلوقتي

  

---

### **Applications that use TCP:**

- HTTP
- FTP → الملفات
- SSH
    - HAS acknowledgement
- SMTP → الميلز

---

![[/Untitled 8 4.png|Untitled 8 4.png]]

- ارمي الداتا ويا أخي عن أمها ما وصلت
    
    ![[/Untitled 9 4.png|Untitled 9 4.png]]
    

  

---

![[/Untitled 10 4.png|Untitled 10 4.png]]

- Applications that use UDP:
    
    - DHCP
        - automatic IPs
    - DNS
    - SNMP
        - Monitring
    - TFTP
    - VoIP
        - الاتصال صوتيا
    - Video Conferencing
    
      
    

---

### Port Numbers

- هو المسؤل انه يفصل مكالمة اخوك مع صحابه عن مكالمتك مع السواق
- used in TCP & UDP
- it’s auto generated from the Source
    - Destination port number → which service you want to access
- Source port number is used as destination when service responses to your request

  

![[/Untitled 11 4.png|Untitled 11 4.png]]

==Socket==

- is the
    - → Combination of the source IP address and source port number ==OR==
    - → Combination of the destination IP address and destination port number.
- Enable multiple processes, running on a client, to distinguish themselves from each other,  
    and multiple connections to a server process to be distinguished from each other. ([[Transportation of Data ( Module 14 )]])

  

![[/Untitled 12 4.png|Untitled 12 4.png]]

- Well-known → الـ Services المعروفة زي ال http مثلا
- Registered → لحاجات معينة
- private → انت اللي بتعمله عشان تبقى ال source port بتاعك

  

  

### TCP Communication Process

![[/Untitled 13 4.png|Untitled 13 4.png]]

- بتبعت للسيرفر بالـ source port بتاعك وال destination port بتاعه، ولما يجي عشان يرد عليك أنت لوحدك، هيعكس، هيخلي الـ source port بتاعك هو ال destination بالنسبة له، وال destination بتاعه هيكون هو ال source port

  

![[/Untitled 14 3.png|Untitled 14 3.png]]

عشان تبدأ الاتصال محتاج تعمل الـ 3 خطوات دول:

3 way handshake

1. أول مرة الأول بيبعت للتاني SYN ويتأكد هل وصل للتاني لا لأ  
    SYN → Synchronization
2. التاني هيبعت للأول SYN, ACK ويتأكد هل وصلوا للأول ولا لأ  
    ACK → Acknowledgment
3. هيتبني بقى ال Establishment ما بينهم ولو في packets هتتبعت بقى

  

![[/Untitled 15 3.png|Untitled 15 3.png]]

عشان تقفل السيشن محتاج تعمل ال 4 خطوات دي

- نفس الفكرة اللي فاتت، ولما ال4 خطوات يخلصوا، الاتصال هيتقطع

  

### Reliability and Flow Control

  

TCP Reliability- Guaranteed and Ordered Delivery

![[/Untitled 16 3.png|Untitled 16 3.png]]

الـ Reliability → الموضوع موثوق فيه، لأن زي في المثال هنا، ترتيب ال segments وصل مختلف -مش الترتيب الصح- لكن كنت متأكد وحصل فعلا أن ال TCP رتبهم بالترتيب المظبوط تاني

ترتيب ال segments قد يختلف لأن مش لازم كلهم يمشوا في نفس ال route فممكن واحدة تسبق التانية

  

TCP Reliability – Data Loss and Retransmission

![[/Untitled 17 3.png|Untitled 17 3.png]]

لو حصل فقد في أي segment, فالمستقبل هيبعت يطلبهم تاني - اللي فُقد بس هو اللي هيتطلب تاني، أما اللي وصل من أول مرة فخلاص هو تمام كدا.

  

TCP Flow Control – Window Size and Acknowledgments

![[/Untitled 18 3.png|Untitled 18 3.png]]

Window Size: Minimum number of bits that could be sent from sender to reciever.

Maximum Segment Size (MSS):

أكتر عدد bits ممكن يتبعت في المرة الواحدة

ممكن السعة اللي المستقبل يقدر يستقبلها في المرة الواحدة تتغير عادي فاشطا يعني، زي الخط الأخضر الثاني والثالث في الصورة كدا

  

TCP Flow Control – Congestion Avoidance

![[/Untitled 19 3.png|Untitled 19 3.png]]

اقرأها 😃

  

---

كلام عن ال UDP نفس الكلام هنا فاشطا