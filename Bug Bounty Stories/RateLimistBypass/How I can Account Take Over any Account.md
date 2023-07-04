# ***How I can Account Take Over any Account ?***

*1. While subdomain enumeration, I found a subdomain (app.dev.Target.com) that was a copy of the main site.* <br>
*2. While browsing the main site, I came accross OTP that was a 4 digit number.* <br>
*3. The first thing that came to my mind was to brute forcing the number. but unfortunately they have rate limit.* <br>
*4. I tried to change IP origin header but it didn't work.* <br>
``` 
X-Originating-IP: 127.0.0.1
X-Forwarded-For: 127.0.0.1
X-Remote-IP: 127.0.0.1
X-Remote-Addr: 127.0.0.1
X-Client-IP: 127.0.0.1
X-Host: 127.0.0.1
X-Forwared-Host: 127.0.0.1
```
*5. I tried to use similar endpoints but it didn't work.* <br>
*6. I tried to add extra param to path but it didn't work.* <br>
*7. I remebered the interesting sub domain (app.dev.Target.com). Why not try it? but it also had rate limit.* <br>
*8. I tried to change IP origin header on app.dev.Target.com. and BOOM :)
So Now I can Take Over any Account Just by knowing the Phone number! Enjoy!*
<br>&nbsp;

----
## ***Credit***
Based on [CyberOz](https://medium.com/@ozomarzu/how-i-can-account-take-over-any-account-b3ce8b50c541)'s writeup.

----
## ***Support***
You can Follow [me](https://www.linkedin.com/in/bhavesh-pardhi-/) on LinkedIn or
<br><br>[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Support-orange?style=for-the-badge&logo=buy-me-a-coffee)](https://www.buymeacoffee.com/bhaveshpardhi)
