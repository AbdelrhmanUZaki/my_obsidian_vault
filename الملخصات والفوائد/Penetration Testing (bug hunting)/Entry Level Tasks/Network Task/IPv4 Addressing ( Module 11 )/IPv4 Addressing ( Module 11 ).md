---
share_link: https://share.note.sx/vdcqzcdf#QbamIbgrQvxzxx/xxYqMZrqEMBSJyvNfal2bo9UDKHU
share_updated: 2023-12-02T22:33:16+02:00
dg-publish: true
---
  

# Part 1

### **IPv4 Address Structure:**

  

`Network & Host Portions:`

  

IPv4 Address is ==32-bit==

- كل ما تزود في عدد ال bits بتاعت ال Host Portion, هتقلل من عدد ال bits Network Portion, **==العلاقة عكسية==**
- Subnet mask: used to identify Network & host portions
- ![[/Untitled 19.png|Untitled 19.png]]
    

---

  

`The Subnet Mask:`

- bit by bit, from left to right
- The actual process is called ==ANDing== (between IPv4 address and Subnet Mask).  
    as shown in this pic
- The result form ANDing is ( 192.168.10.0 )
    
    ![[/Untitled 1 8.png|Untitled 1 8.png]]
    
    - توضيح لعملية ال ANDing
        
        ![[/Untitled 2 9.png|Untitled 2 9.png]]
        
- Every number represent is binary with 8 bits

  

The Prefix Length

- عدد الوحايد  
    
    ![[/Untitled 3 7.png|Untitled 3 7.png]]
    

---

- ==$\text {Number of hosts}= 2^h - 2$==﻿ ==, h: number of bits of Host Portion.==بنطرح $2 $﻿ هنا عشان واحدة منهم لل Network address  
    والتانية لل Broadcast address  
    - ==$0$==﻿ for Network address  
    - ==$255 $==﻿ for Broadcast address
- ==$\text {Number of networks} = 2^n$==﻿==, n: number of bits of network/subnets.  
    ==

- addresses start ==from 0 To 254== , and the probability of numbers is ==$2^8$==﻿ which is ==$255$==﻿

![[/Untitled 4 6.png|Untitled 4 6.png]]

---

`Unicast, Broadcast and Multicast:`

Multicast: Using IP Group

- كل عنصر هيكون له نفس الرقم بالظبط، ال IP Group يعني

---

`Public and Private IPv4 Addresses:`

- عملنا ال Private دي عشان ال Public IPs عددها أقل من عدد البشر أصلا  
    وعشان كدا بنستخدم [[IPv4 Addressing ( Module 11 )]], البيت كله هيكون له real/Global IP واحد بس
- Private addresses —> internal hosts

---

`Routing to the Internet:`

- NAT ( Network Address Translation ) : Translate Private IPv4 addresses to public/global/real IPv4 addresses

---

`Special Use IPv4 Addresses:`

  

- Loopback: دا عشان تبعت الرسالة لنفسك، ولما توصل لك فعلا هتتأكد أن لو ال Host بقى أونلاين، هيقدر يبعت ويستقبل عادي

![[/Untitled 5 6.png|Untitled 5 6.png]]

---

For Test cases, not in real use ( يوس 😄)

![[/Untitled 6 4.png|Untitled 6 4.png]]

منظمة عيانة IANA هي اللي بتنظم توزيع ال IPs في العالم

---

### Network Segmentation: —> subnetting

- `Broadcast Domains and Segmentation`
    
    ![[/Untitled 7 4.png|Untitled 7 4.png]]
    
    ---
    
- `Problems with Large Broadcast Domains`
    
    ![[/Untitled 8 3.png|Untitled 8 3.png]]
    
    ---
    
    `Reasons for Segmenting Networks`
    
- الهدف أنك تقلل ال broadcast domain عشان عدد الأجهزة هيكون كتيييير  
    عن طريق أنك هتقسم الأجهزة لمجموعات
- Subnetting reduces overall network traffic and improves network performance.
- It can be used to implement security policies between subnets.
- Subnetting reduces the number of devices affected by abnormal broadcast traffic
- ![[/Untitled 9 3.png|Untitled 9 3.png]]
    

---

### Subnet an IPv4 Network

  

`Subnet on an Octet Boundary`

  

هنا هتتوضح العلاقة العكسية ما بين عدد ال Hosts وعدد ال Networks  
n —> Network, h —> Host

![[/Untitled 10 3.png|Untitled 10 3.png]]

![[/Untitled 11 3.png|Untitled 11 3.png]]

  

![[/Untitled 12 3.png|Untitled 12 3.png]]

---

  

`Subnet a Slash 16 and a Slash 8 Prefix`

- ![[/Untitled 13 3.png|Untitled 13 3.png]]
    
- ![[/Untitled 14 2.png|Untitled 14 2.png]]
    

$\text{To create a 100 subnet, you need to satisfy the requirments of it with this equation,~~~}\\{x~}->\text{number of total subnets which here will be 128}\\2^x -2 >= 100$﻿

- عشان تحسب هتحتاج تستلف اد اي، لازم تستلف عدد أكبر من عدد ال subnets اللي هو طالبه عشان تقدر توفيه

---

`Subnet to Meet Requirements`

![[/Untitled 15 2.png|Untitled 15 2.png]]

---

---

# Part 2

  

### **Variable Lenght Subnet Mask (VLSM)**

  

- المسألة اللي في الفيديو

![[/Untitled 16 2.png|Untitled 16 2.png]]

  

- محتوى أول 12 دقيقة من الفيديو - ==Subnet 1==

![[/Untitled 17 2.png|Untitled 17 2.png]]

  

- ==Subnet 2==
    
    ![[/Untitled 18 2.png|Untitled 18 2.png]]
    

  

- ==Subnet 3 & 4==

![[/Untitled 19 2.png|Untitled 19 2.png]]

  

- ==Subnet 5==

![[Untitled 20.png]]

  

  

  

  

  

  

  

Video part 2

[https://www.youtube.com/watch?v=ngPYDnsVpBY&list=PLPBnj6azlABanyaILYOT0FKKtcSoeOc2A&index=13](https://www.youtube.com/watch?v=ngPYDnsVpBY&list=PLPBnj6azlABanyaILYOT0FKKtcSoeOc2A&index=13)