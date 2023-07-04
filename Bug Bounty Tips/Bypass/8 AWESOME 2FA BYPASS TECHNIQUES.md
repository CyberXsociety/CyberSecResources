# *𝟏. 𝐀𝐜𝐜𝐞𝐬𝐬 𝐍𝐞𝐱𝐭 𝐄𝐧𝐝𝐩𝐨𝐢𝐧𝐭 𝐃𝐢𝐫𝐞𝐜𝐭𝐥𝐲*

*⪼ Just try to access the next endpoint directly (you need to know the path of the next endpoint)*

*⪼ If this doesn't work, try to change the Referrer header as if you came from the 2FA page.*

# *𝟐. 𝐒𝐡𝐚𝐫𝐢𝐧𝐠 𝐔𝐧𝐮𝐬𝐞𝐝 𝐂𝐨𝐝𝐞*

*⪼ Check if you can get for your account a token and try to use it to bypass the 2FA in a different account.*

# *𝟑. 𝐋𝐞𝐚𝐤𝐞𝐝 𝐂𝐨𝐝𝐞*

*⪼ Is the token leaked on a response from the web application?*

# *𝟒. 𝐏𝐚𝐬𝐬𝐰𝐨𝐫𝐝 𝐑𝐞𝐬𝐞𝐭 𝐅𝐮𝐧𝐜𝐭𝐢𝐨𝐧*

*⪼ In almost all web applications the password reset function automatically logs the user into the application after the reset procedure is completed.*

# *𝟓. 𝐑𝐞𝐮𝐬𝐞 𝟐𝐅𝐀 𝐂𝐨𝐝𝐞*

*⪼ Also, try requesting multiple 2FA codes and see if previously requested Codes expire or not when a new code is requested*

# *𝟔. 𝐁𝐫𝐮𝐭𝐞 𝐅𝐨𝐫𝐜𝐞*

*⪼ There is any limit in the amount of codes that you can try, so you can just brute force it.*

# *𝟕. 𝐑𝐞𝐬𝐩𝐨𝐧𝐬𝐞 𝐌𝐚𝐧𝐢𝐩𝐮𝐥𝐚𝐭𝐢𝐨𝐧*

*⪼ Change failed response to success response*

*⪼ Change failed status code to success status code*

# *𝟖. 𝐑𝐚𝐭𝐞 𝐋𝐢𝐦𝐢𝐭 𝐁𝐲𝐩𝐚𝐬𝐬*

*⪼ Using Similar Endpoints: /sign-up --> /Sign-up*

*⪼ Blank char in params: code=1234%0a*

*⪼ Change Origin IP using header: X-Forwarded-For: 127.0.0.1*

*⪼ Add extra params: /resetpwd?someparam=1</br>*

----
# ***Support***
You can Follow [me](https://www.linkedin.com/in/bhavesh-pardhi-/) on LinkedIn or
<br><br>[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Support-orange?style=for-the-badge&logo=buy-me-a-coffee)](https://www.buymeacoffee.com/bhaveshpardhi)
