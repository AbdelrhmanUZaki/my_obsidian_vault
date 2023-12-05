---
share_link: https://share.note.sx/v5c2zlqy#3OMoSKnZWjXueGhla/Sm8KIuQWUKxcSIqJkgBiJpoPs
share_updated: 2023-12-03T23:18:28+02:00
dg-publish: true
---
  

# Task 5

  

- use `ls` command to show the content of the folder you are in ‘tryhackme’ folder.
    - you will find that they are **4 folders**

  

- use `ls` command till i found one that has a file inside.
    - the folder is **‘folder4’**

  

- To read text file content you need to do:
    - entering folder that have the file with command: `cd folder4`
    - read text file contect with this command: `cat note.txt`
    - You will find this text there **Hello World!**

  

- To know a full path to the text file you need to do:
    
    - Use `cd folder4` to enter folder4 folder
    - Use `pwd` to know the path where **note.txt** file exist
    - The path is:  
        /home/tryhackme/folder4
    
      
    
    ---
    
      
    
    # Task 6
    
- To find the flag you need:
    - To find a word in a text you need to use `greb` command followed by the word you search for followed by file name with its extension.
    - as shown here:
        - `grep THM access.log`
        - you will find the flag **THM{ACCESS}**

  

---

# Task 7

- To run a command in background Use `&` operator after the command separated by space.

  

- To replace the content of a file named "passwords" with the word "password123", you need to:
    - Use `echo password123` to write ‘password123’
    - Use `> passwords` to store output in the lefthand side as an input for the righthand side which is our file “passwords”.
    - Using `>` operator, this will write over the data, and old data -text- will be lost, and this what we want
    - combine two steps as this:
        
        - `echo password123 > passwords`
        
          
        
- Now if I want to add "tryhackme" to this file named "passwords" but also keep "passwords123", you need to:
    - Use `echo tryhackme` command to write ‘tryhackme’
    - Use `>> passwords` to store output in the lefthand side as an input for the righthand side which is our file “passwords”.
    - Using `>>` operator, this will append a new text below the old text, old data will not be lost’
    - combine steps as this:
        
        - `echo tryhackme >> passwords`