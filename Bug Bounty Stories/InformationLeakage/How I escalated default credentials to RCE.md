# ***How I escalated default credentials to RCE 🧯***

*1. I came across an application which was using Tomcat.* <br>

*2. The first thing I did was brute forcing tomcat directories, but unfortunately, it did not work.* <br>

*3. I tried a couple of more things but it didn’t work, that’s where I decided to visit Shodan.* <br>

*4. I saw some application running on port 8082 and it was using tomcat.* <br>

*5. I tried accessing `http://x.x.x.x:8082/manager` and guess what, it was prompting me to enter username and password.* <br>

*6. BOOM!!!!!, The username=tomcat and password=s3cret worked and the Tomcat Application Manager Console was accessible.* <br>

*7. I should have stopped but I knew, I can get a remote code execution by uploading malicious war file.* <br>

*8. I created the WAR file with malicious JSP file.* <br>

*9. I navigated to “Select WAR file to upload” section and uploaded it.* <br>

*10. The webshell was successfully uploaded and I was able to run a few commands on it.*
<br>&nbsp;

----
## ***Credit***
Based on [Pawan Chhabria](https://infosecwriteups.com/how-i-escalated-default-credentials-to-remote-code-execution-1c34504be7a5)'s writeup.

----
## ***Support***
You can Follow [me](https://www.linkedin.com/in/bhavesh-pardhi-/) on LinkedIn or
<br><br>[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Support-orange?style=for-the-badge&logo=buy-me-a-coffee)](https://www.buymeacoffee.com/bhaveshpardhi)