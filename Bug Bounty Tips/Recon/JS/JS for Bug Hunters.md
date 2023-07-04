# ***JS for Bug Hunters 🛹***

## *Items You Should Be Searching For:*
*1. New Endpoints* <br>
*2. New Parameters* <br>
*3. Hidden Features* <br>
*4. API Keys* <br>
*5. Developer Comments* <br>
```
cat *js | grep -r -E "aws_access_key|aws_secret_key|api key|passwd|pwd|heroku|slack|firebase|swagger|aws_secret_key|aws key|password|ftp password|jdbc|db|sql|secret jet|config|admin|pwd|json|gcp|htaccess|.env|ssh key|.git|access key|secret token|oauth_token|oauth_token_secret" /path/to/directory/*.js
```

## *How to Extract JS File:*
*1. Discover subdomains* <br> 
*2. Find live subdomains* <br>
*3. Retrieves historical URLs* <br>
*4. Filter URLs that contain ".js"* <br> 
```
subfinder -d domain.com | httpx -mc 200 | tee subdomains.txt && cat subdomains.txt | waybackurls | httpx -mc 200 | grep .js | tee js.txt
```

## *Use Nuclei Exposures Tag*
```
nuclei -l js.txt -t ~/nuclei-templates/exposures/ -o js_exposures_results.txt
```
<br>&nbsp;

----
## ***Credit***
Based on [Shrirang Diwakar](https://shrirangdiwakar.medium.com/bypassing-403s-like-a-pro-2-100-broken-access-control-66beef4afa8c)'s writeup.
<br>&nbsp;

----
## ***Support***
You can Follow [me](https://www.linkedin.com/in/bhavesh-pardhi-/) on LinkedIn or
<br><br>[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Support-orange?style=for-the-badge&logo=buy-me-a-coffee)](https://www.buymeacoffee.com/bhaveshpardhi)
