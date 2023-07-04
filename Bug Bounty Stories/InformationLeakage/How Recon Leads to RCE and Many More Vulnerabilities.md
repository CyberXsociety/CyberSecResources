# ***How Recon Leads to RCE and Many More Vulnerabilities 🩻***

*1. I started with basic subdomain enumeration using tools*
```
$ subfinder -d redacted.com -o subfinder.txt
$ amass enum -d --passive redacted.com -o amass.txt
$ echo redacted.com | assetfinder --subs-only | tee assetfinder.txt
$ cat subfinder.txt amass.txt assetfinder.txt | sort -u | anew subdomains.txt
$ cat subdomains.txt | alterx | anew subd.txt
```
*2. Now, its time to resolve the subdomains and check how many of them are alive or having status code 200.*
```
$ cat subd.txt | httpx -mc 200 | tee live.txt
```
*3. I found that subdomain’s endpoint /teamlevelis hosting the information of all its employees in a hierarchy format.*  <br>

*4. I found that the subdomain itself leaking the PII data of its employees.* <br>

*5. I started fuzzing the subdomain and found an interesting endpoint /hrms which is asking for the employee’s email address to login/authorize.* <br>

*6. I entered an email ID and without any password or OTP, I logged into their dashboard and was allowed to change the data available on it.* <br>

*7. I started playing with input boxes and first thing I tried inputting a XSS payload `<img src=x onerror=prompt()>` in all froms and submit it. and BOOM* <br>

*8. I logged into the dashboard and found file upload functionality. I have tried to upload a php file and BOOM*
<br>&nbsp;

----
## ***Credit***
Based on [ar_hawk](https://medium.com/@ar_hawk/how-a-simple-directory-listing-leads-to-pii-data-leakage-remote-code-execution-and-many-more-104b09e644f4)'s writeup.

----
## ***Support***
You can Follow [me](https://www.linkedin.com/in/bhavesh-pardhi-/) on LinkedIn or
<br><br>[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Support-orange?style=for-the-badge&logo=buy-me-a-coffee)](https://www.buymeacoffee.com/bhaveshpardhi)