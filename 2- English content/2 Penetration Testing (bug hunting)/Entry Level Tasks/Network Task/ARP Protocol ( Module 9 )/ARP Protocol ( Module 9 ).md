---
share_link: https://share.note.sx/bgmwo99j#1Qdci561sg27hCvGNyLJbHKOCyYVxvdfl8SnLNyvxZo
share_updated: 2023-12-02T22:33:11+02:00
dg-publish: true
---
  

### MAC and IP:

  

  

![[/Untitled 18.png|Untitled 18.png]]

  

---

`Destination on Remote Network:`

when the destination IP address is on a remote network, the destination MAC address is that of the default gateway.

- _==ARP==_ is used by ==_IPv4_== to associate the IPv4 address of a device with the MAC address of the device _NIC_
- ==_ICMPv6_== is used by ==_IPv6_== to associate the IPv6 address of a device with the MAC address of the device _NIC_.

— ال ARP بيبعت لكل اللي معاه في الشبكة ولما يلاحظ الجهاز اللي بيطابق ال IP اللي عنده اللي هو باعت الرسالة عشانه أصلا، بياخد ساعتها ال MAC Address بتاعه ويضيفه في ال Packet، بعدين يبعت ال Packet كاملة للجهاز دا —  
بيعمل كدا عشان لازم يكون عارف ال MAC Address للجهاز اللي هيبعتله الرسالة اللي عايزها توصل له

![[/Untitled 1 7.png|Untitled 1 7.png]]

  

- ==_ICMPv6_== is the same like ==_ARP_== but it is used with ==_IPv6_==

---

  

`ARP Functions:`

- حالات مهمة اقرأها
    
    ![[/Untitled 2 8.png|Untitled 2 8.png]]
    

---

  

`Removing Entries from an ARP Table:`

ARP table  
- مش دايمة  
- مدة بقاء ال ARP cache بتختلف حسب ال OS  
- ممكن تشيل عناصر ال ARP table يدويا

![[/Untitled 3 6.png|Untitled 3 6.png]]

---

  

`ARP Issues - ARP Broadcasting and ARP Spoofing :`

- لو في ==Attacker== دخل على الشبكة ممكن يعمل نفسه هو الجهاز اللي أنا عايز منه MAC address بتاعه  
    فلما أبعت البيانات -رسالة الداتا- بعد ما خدت ال MAC Address, هتوصل له وهيسرقها كدا
- بتاخد وقت كتير عما تبعت الرسالة -ARP Request - لكل الأجهزة اللي على الشبكة
- Enterprise level switches include mitigation techniques to protect against ARP attacks. | في بعض التيكنيكس اللي بتحاول تصد ال Attacker هنا