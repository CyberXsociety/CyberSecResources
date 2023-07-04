# ***IDOR leading to Privilege Escalation! 🪰***

*1. I quickly went to the password reset section* <br>
*2. After entering a new password in both input fields, I captured the request.* <br>
*3. The parameters were not so interesting to me, also I check them for other bugs but no success :(* <br>
*4. Anyways I saw a header named “uid” which had my current email.* <br>
*5. I simply created another account and replaced my email inside the “uid” header with this victim mail.* <br>
*6. BOOM!! We just changed the victim’s password!!*
<br>&nbsp;

----
## ***Credit***
Based on [Kapil Varma](https://k4pil.medium.com/idor-leading-to-privilege-escalation-c45f4a6380a1)'s writeup.
<br>&nbsp;

----
## ***Support***
You can Follow [me](https://www.linkedin.com/in/bhavesh-pardhi-/) on LinkedIn or
<br><br>[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Support-orange?style=for-the-badge&logo=buy-me-a-coffee)](https://www.buymeacoffee.com/bhaveshpardhi)
