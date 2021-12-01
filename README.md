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

2. Tools / Sites  
   - [csp evaluator](https://csp-evaluator.withgoogle.com/)  
   - [certificate transparency log](https://crt.sh/) 
   - [hash cracker](https://crackstation.net/)
   - [base64 decoder/encoder](https://www.base64decode.org/)
 
