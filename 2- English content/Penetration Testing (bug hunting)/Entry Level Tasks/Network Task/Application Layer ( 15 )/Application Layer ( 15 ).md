---
share_link: https://share.note.sx/ixbfwiux#OD87GCkOonQG7MATqPY77Byc0aSB9DL1K8l5jdfSJZA
share_updated: 2023-12-02T22:33:19+02:00
dg-publish: true
---
Simple Mail Transfer Protocol (SMTP)  
– used to send mail.  
• Post Office Protocol (POP) & IMAP –  
used for clients to receive mail.

  

## Application Layer

The application layer provides the interface between the applications used to communicate, and the underlying network over which messages are transmitted.

- application layer protocols:
    
    - HTTP
    - FTP
    - TFTP
    - IMAP
    - DNS
    
      
    

![[/Untitled 22.png|Untitled 22.png]]

---

  

## Presentation and Session Layer

  

- Formatting, or presenting
- Compressing data
- Encrypting data

  

### The session layer functions:

- بتعمل الـ connection
- مسؤولة انها تخلي السيشن active علطول
- مسؤولة عن نقل الداتا، وبتrestart السيشن تاني لو حصل فيها مشكلة

![[/Untitled 1 10.png|Untitled 1 10.png]]

---

  

![[/Untitled 2 11.png|Untitled 2 11.png]]

---

  

## ==Peer-to-Peer==

  

![[/Untitled 3 9.png|Untitled 3 9.png]]

`Client-Server Model`

اللي بيطلب هو الـ client

اللي بيرد هو الـ server

---

`Peer-to-Peer Networks`

![[/Untitled 4 8.png|Untitled 4 8.png]]

أكتر من جهاز متصلين ببعض عن طريق الشبكة ويقدروا يشاركوا Resources زي الطابعة مثلا… منغير حتى ما يكون في server

---

`Peer-to-Peer Applications`

Ex: WhatsApp application

---

`Common P2P Applications`

لو جهاز في الشبكة محتاج حاجة، وكل جهاز تاني في الشبكة عنده جزء/الحاجة دي، فأنت ممكن من كل جهاز تاخد حتة

Ex: BitTorrent 😄

---

## ==Web and Email Protocols==

`Hypertext Transfer Protocol and Hypertext Markup Language`

  

Uniform Resource Locator (URL) → سموه كدا عشان هو اللي بيحدد الموقع بيكون موجود فين بالظبط

==Step 1==

The browser interprets the three parts of the URL:

1. http (the protocol or scheme)
2. [www.cisco.com](http://www.cisco.com/) (the server name)
3. index.html (the specific filename requested) -كان الزيرو قالها في كورس الويب بتاعه، أن السيرفر بيبدأ أول حاجة أنه يدور على الملف اللي اسمه index-

==Step 2==

1. The browser then checks with a name server(==DNS==) to convert [www.cisco.com](http://www.cisco.com/) into a numeric IP address  
    which it uses to connect to the server.
2. The client initiates an HTTP request to a server by sending a ==GET== request to the server and asks for the index.html file.

==Step 3==

In response to the request, the server sends the HTML code for this web page to the browser.

==Step 4==

The browser deciphers (بتفهم/ بتترجم) the HTML code and formats the page for the browser window.

---

`HTTP and HTTPS`

Common message types:

1. ==GET:==
    1. This is a client request for data. A client (web browser) sends the GET message to the web server to request HTML pages.
2. ==POST==
    1. This uploads data files to the web server, such as form data.
3. ==PUT==
    
    1. This uploads resources or content to the web server, such as an image
    
      
    

---

`Email Protocols`

1. Simple Mail Transfer Protocol (==SMTP==)
    1. used to ==send== mail.
2. Post Office Protocol (==POP==) & ==IMAP==
    1. used for clients to ==receive== mail.
        1. POP → doesn’t store messages, while it has been sent, it’s deleted form the server
        2. IMAP → Store it

---

## IP Addressing Services

  

`Domain Name Serivce ( DNS )`

  

![[/Untitled 5 8.png|Untitled 5 8.png]]

`DNS Hierarchy`

  

![[/Untitled 6 6.png|Untitled 6 6.png]]

---

`Dynamic Host Configuration Protocol ( DHCP )`

![[/Untitled 7 6.png|Untitled 7 6.png]]

بتستخدمه عشان لو عندك شبكات كتير، بدل ما تعمل كل IP يدوي كدا، هو هيعمله اوتوماتيك بدالك

لازم يكون في offer و request بالقبول عشان ال client ياخد ال IP

لي لازم؟

عشان ال client ممكن يكون حوالي أكتر من DHCP Server فلما الـ client يبعت Request، كلهم هيردوا عليه ويعرضوا عليه ال IPs، فهو لازم يقبل واحد بس، مهي الدنيا مش سبهللة كدا برضو!

---

## File Sharing Services

`File Transfer Protocol`

![[/Untitled 8 5.png|Untitled 8 5.png]]

Step 1:

client establishes the first connection to the server for control traffic using TCP ==port 21.==

Step 2:

client establishes the ==second== connection to the server for the ==actual data transfer== using TCP ==port 20==.

Step 3:

The data transfer can happen in either direction.

The client can ==download== (==pull==) data from the server,

or the client can ==upload== (==push==) data to the server.

---

`Server Message Block (SMP)`

![[/Untitled 9 5.png|Untitled 9 5.png]]

باختصار هو زي برنامج TeamViewer

لمزيد من التفاصيل:

اقرأ السلايد دي