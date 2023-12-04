---
share_link: https://share.note.sx/7mpmwk9l#Yi1t47V6Q/Rav9Ial8ZicnPOhpWWW166OuV5Yyxfa5w
share_updated: 2023-12-04T08:11:50+02:00
dg-publish: true
---
  

# BAC

### First writeup

[https://medium.com/@bag0zathev2/how-i-used-js-files-inspection-and-fuzzing-to-do-admins-supports-stuff-dd4f700605a](https://medium.com/@bag0zathev2/how-i-used-js-files-inspection-and-fuzzing-to-do-admins-supports-stuff-dd4f700605a)

  

— Points Learned

  

1. You always have to check the JS file.
2. Each account has a specific token, but each endpoint is calling that token with a different name.
3. Search for some of Burpsuite extensions, it will be helpful.
4. Try to bypass forbidden functions that only available to website/org Admins.

  

---

  

### Second writeup

[https://medium.com/bugbountywriteup/how-did-i-leak-5-2k-customer-data-from-a-large-company-via-broken-access-control-709eb4027409](https://medium.com/bugbountywriteup/how-did-i-leak-5-2k-customer-data-from-a-large-company-via-broken-access-control-709eb4027409)

  

— Points Learned

  

1. check JS files 😃
2. use tool like `linkfinder` that finds endpoints in JavaScript files.
3. Try to access admin panel -even you don’t have credentials to log in- if you found their endpoint somewhere like JS files and success to see this page. don’t forget to look around and see what you are able to do there.

  

---

  

### Third wirteup

[https://medium.com/@thelinuxboy/30-minute-heist-how-i-bagged-a-1500-bounty-in-just-few-minutes-48753eb2028e](https://medium.com/@thelinuxboy/30-minute-heist-how-i-bagged-a-1500-bounty-in-just-few-minutes-48753eb2028e)

  

— Points Learned

  

1. Take a look about logical bugs.
2. Create two accounts, one as admin, other one is an original user, upgrade original user to be an admin, downgrade him, check if he could still do admin rights
3. Explain in detail the impact of vulnerability you found

# IDOR

### First Writeup

[https://shahjerry33.medium.com/idor-inside-the-session-storage-88af485fc899](https://shahjerry33.medium.com/idor-inside-the-session-storage-88af485fc899)

  

— Points Learned

1. look at session storage in your web browser, manipulate with id or anything that belongs to specific user

  

---

  

### Second Writeup

[https://medium.com/@swapmaurya20/a-simple-idor-to-account-takeover-88b8a1d2ec24](https://medium.com/@swapmaurya20/a-simple-idor-to-account-takeover-88b8a1d2ec24)

  

— Points Learned

  

1. look at body request and check if you could change your data with another user while using functions like “forget my password”, you might get account takeover 😄  
    do this to your other account while you hunt, to avoid harm website users  
    
    ![[الصور والملفات/Untitled 3.png|Untitled 3.png]]
    

  

---

  

### Third Writeup

[https://medium.com/@nynan/what-i-learnt-from-reading-220-idor-bug-reports-6efbea44db7](https://medium.com/@nynan/what-i-learnt-from-reading-220-idor-bug-reports-6efbea44db7)  

  

— Points Learned

1. **Where do are IDORs commonly found?**

1. REST APIs 31.8%
2. GET parameters 25.8%
3. POST request bodies 21.2%
4. graphQL endpoints 9.1%
5. PUT parameters 4.5%
6. IDs in the request header 3.0%
7. IDs in the cookies 3.0%
8. Misc Query languages 1.5%

1. **Some points to keep in mind:**
    1. Is the ID encoded or not in plaintext?
    2. Can a file/resource be accessed directly from the URL, without needing prior authentication?  
        Images are commonly vulnerable to this kind of vulnerability.
    3. Does the exploit involve using a different method?
    4. Sometimes the IDOR can be exploited via a username or email change instead of an ID.
    5. Does it leak PII?
    6. Can you bypass payment?
    7. Can you do actions on other’s behalfs?
    8. Can you destroy or damage any assets or info?
2. Summary
    
    - IDOR bugs are broader than most people think.
    - **Almost 80% of IDORs** are found in REST APIs, GET parameters or POST request bodies, although you should still search in the other 20%.
    - Success in finding IDORs comes from **creative ways** of finding them.
    - Your goal is **not always** to get P1 Account takeovers.