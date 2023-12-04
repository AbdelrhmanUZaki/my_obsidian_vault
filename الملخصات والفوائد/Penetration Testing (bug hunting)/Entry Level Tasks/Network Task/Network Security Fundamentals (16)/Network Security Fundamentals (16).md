---
share_link: https://share.note.sx/nkpnns96#KGKhhExd7yZF0nqX6qgBN9sOkLh0+fE70h8FJDA9mco
share_updated: 2023-12-02T22:33:21+02:00
dg-publish: true
---
  

![[/Untitled 23.png|Untitled 23.png]]

  

## Security Threats and Vulnerabilities

  

### Types of Vulnerabilities

1. ==Technological Vulnerabilities==
    1. might include TCP/IP Protocol weaknesses,
    2. Operating System Weaknesses,
    3. and Network Equipment weaknesses.
2. ==Configuration Vulnerabilities==
    1. might include unsecured user accounts, system accounts with easily guessed passwords, misconfigured internet services, unsecure default settings, and misconfigured network equipment.
3. ==Security Policy Vulnerabilitie==s
    1. might include lack of a written security policy, politics, lack of authentication continuity, logical access controls not applied, software and hardware installation and changes not following policy, and a nonexistent disaster recovery plan.

---

### Physical Security

1. ==Hardware threats==
    1. This includes physical damage to servers, routers, switches, cabling plant, and workstations.  
        
2. ==Environmental threats==
    1. This includes temperature extremes (too hot or too cold) or humidity extremes (too wet or too dry).
3. ==Electrical threats==
    1. This includes voltage spikes, insufficient supply voltage (brownouts), unconditioned power (noise), and total power loss.
4. ==Maintenance threats==
    1. This includes poor handling of key electrical components (electrostatic discharge), lack of critical spare parts, poor cabling, and poor labeling

---

## Network Attacks

### Types of Malwares

1. ==Viruses==
    1. مش هيشتغل إلا لما تشغله أنت بايدك
2. ==Worms==
    1. بيشتغل تلقائي أول ما يوصل جهازك
3. ==Trojan Horses==

---

### Reconnaissance Attacks

1. ==Reconnaissance attacks==
    1. The discovery and mapping of systems, services, or vulnerabilities.
2. [[Network Security Fundamentals (16)]]
    1. The unauthorized manipulation of data, system access, or user privileges.
3. [[Network Security Fundamentals (16)]] ==( DOS )==
    1. The disabling or corruption of networks, systems, or services.

---

### Access Attacks

1. ==Password attacks==
    1. brute force
    2. trojan horse
    3. packet sniffers
2. ==Trust exploitation==
    1. A threat actor uses unauthorized privileges to gain access to a system, possibly compromising the target.
3. ==Port redirection==:
    1. A threat actor uses a compromised system as a base for attacks  
        against other targets.
        1. For example, a threat actor using SSH (port 22) to connect to a compromised host A. Host A is trusted by host B and, therefore, the threat actor can use Telnet (port 23) to access it.
4. ==Man-in-the middle==:
    1. هيقف في الطريق بينك والمستقبل عشان يعدل على الداتا دي ويبعتها للمستقبل، وهكذا، لما المستقبل يبعت لك حاجة، هو هيلعب فيها برضو

---

### Denial of Service Attacks

1. DoS attacks take many forms.
    1. They prevent authorized people from using a service by consuming system resources.
    2. To help prevent DoS attacks it is important to stay up to date with the latest security updates for operating systems and applications.
2. DoS attacks are a major risk because they interrupt communication and cause significant loss of time and money.
    1. These attacks are relatively simple to conduct, even by an unskilled threat actor.
3. A DDoS is similar to a DoS attack, but it originates from multiple, coordinated sources.
    1. For example
        1. a threat actor builds a network of infected hosts, known as ==zombies (==**==botnet==**==)==.
        2. The threat actor uses a command and control (CnC) program to instruct the botnet of zombies to carry out a DDoS attack

---

## Network Attack Mitigations

### The Defense-in-Depth Approach

1. VPN
2. ASA Firewall
3. IPS
4. ESA/WSA
5. AAA Server ()

---

### Keep Backups

![[/Untitled 1 11.png|Untitled 1 11.png]]

---

### Upgrade, Update, and Patch

Patch → تحسين/ إصلاح

خلي دايما الويندوز عندك متحدث لآخر حاجة عشان التحديثات دي بتكون ترقيع لثغرات ظهرت فبيلحقوا نفسهم

---

### Authentication, Authorization, and Accounting

- Authentication:
    - مين الشخص اللي دخل؟
- Authorization
    - اي صلاحيات الشخص دا؟
- Accounting
    - تسجيل كل حاجة الشخص عملها (logs)

---

### Firewalls

![[/Untitled 2 12.png|Untitled 2 12.png]]

### Types of Firewalls:

1. ==Packet filtering==
    1. Prevents or allows access based on IP or MAC addresses  
        يحجب جهاز معين
2. ==Application filtering==
    1. Prevents or allows access by specific application types based on port numbers  
        يحجب بورتات معينة، فمثلا لو حجبت Port 80  
        كدا مش هتعرف تخش على أي موقع خالص/ مش هتكون متوصل بالنت
3. ==URL filtering==
    1. Prevents or allows access to websites based on specific URLs or keywords  
        يحجب مواقع معينة
4. ==Stateful packet inspection== (SPI)
    1. Incoming packets must be legitimate responses to requests from internal hosts. Unsolicited packets are blocked unless permitted specifically. SPI can also include the capability to recognize and filter out specific types of attacks, such as denial of service (DoS).
        
        هسألك سؤال، ولو جاوبت صح هتعرف تدخل