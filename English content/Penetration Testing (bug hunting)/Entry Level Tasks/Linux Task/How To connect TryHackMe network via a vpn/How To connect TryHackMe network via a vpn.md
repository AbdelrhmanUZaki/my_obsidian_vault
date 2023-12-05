---
share_link: https://share.note.sx/7yccdaaw#atmMamBPFMK1gxdi7qvxMILFQecZc8HGAHV/lxfsuUo
share_updated: 2023-12-04T08:10:38+02:00
dg-publish: true
---
to access TryHackMe (THM) machines in your Linux machine

  

## This is my steps to use my machine to access THM labs without using attackbox.

  

### First Download your needed files

1. Download this vpn [1.1.1.1](https://1.1.1.1/) (in your windows not in virtual machine) and setup it.  
    

![[Untitled 26.png|Untitled 26.png]]

  

1. Download your Configuration file from this link [TryHackMe | Network Access](https://tryhackme.com/access) (in Linux in virtual machine)  
    
    ![[Untitled 1 13.png|Untitled 1 13.png]]
    
      
    
2. Write these commands in Linux’s terminal to install openvpn
    
    `sudo apt-get update`
    
    `sudo apt-get upgrage`
    
    `sudo apt-get install openvpn`
    

---

  

### Second:

steps to connect

1. open [[How To connect TryHackMe network via a vpn]] in windows, and make a connection (press the button in the middle of the app)  
    in Linux type `warp-cli connect`

Before

![[Untitled 2 14.png|Untitled 2 14.png]]

After

![[Untitled 3 11.png|Untitled 3 11.png]]

  

1. in terminal write:

`sudo openvpn` and beside it,(drag and drop configuration file)

drag and drop this file OR write file’s path in Linux, it’s the same thing

so, for example if my username in THM is ‘abdelrahman112’, then command line will be: `sudo openvpn abdelrahman112.ovpn`

It will not be actually like that because i didn't write the full path to the file cause i don't have one now but anyway you got it :)

-update with ex: command after you drop it would be like ==**sudo openvpn '/home/USER_NAME/Downloads/abdelrahman112.ovpn’**==

1. Wait just seconds until you see ‘intialization sequence completed’ in your terminal and then Disconnect this [[How To connect TryHackMe network via a vpn]] (in Linux type `warp-cli disconnect`) and **==Don’t==** close the terminal that your wrote last command in.
2. Go to your room in THM to get your machine’s IP as shown below in pic

![[Untitled 4 10.png|Untitled 4 10.png]]

and write this command in another terminal (you can use ‘==ctrl+Shift+T==’ to open another one), and note that in this room, machine’s username is ‘tryhackme’ so command will be like that:  
`ssh tryhackme@Your_machine_ip`

its general form is: `ssh Username@MACHINE_IP`

![[Untitled 5 9.png|Untitled 5 9.png]]

  

Every time you want to access THM in linux in your virutal machine, you will need to do the 'Second part' Steps

([[How To connect TryHackMe network via a vpn]])

  

$\large \text {Enjoy!!}$