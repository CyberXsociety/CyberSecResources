# ***IDOR a Highest Bounty 🍺***

*1. I used google dorks for recon the website.*
```
site:*.example.com inurl:.aspx
```
*2. In the result, the user data has been leaked and URL is like this*
```
https://buy.example.com/protect/landing.aspx?base64encodeddata
```
*3. This base64 encoded data is a user’s mobile number by which a user is validated.* <br>
*4. I changed the mobile number to other user’s mobile number and BOOM!* <br>
*5. this Vulnerability gives me 2000$ and the severity of this bug is P0* 
<br>&nbsp;

---
## ***Credit***
Based on [omdubey170](https://medium.com/@omdubey170/idor-a-highest-bounty-6dae1bb10b66)'s writeup.

----
## ***Support***
You can Follow [me](https://www.linkedin.com/in/bhavesh-pardhi-/) on LinkedIn or
<br><br>[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Support-orange?style=for-the-badge&logo=buy-me-a-coffee)](https://www.buymeacoffee.com/bhaveshpardhi)