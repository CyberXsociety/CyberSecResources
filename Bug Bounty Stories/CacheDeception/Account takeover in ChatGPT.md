# ***Account Takeover in ChatGPT***

*1. We could access* `https://chat.openai.com/api/auth/session` and the API will return our account data, such as name, email, ID, and the most critical one: our access token.

*2. Now if we go to* `https://chat.openai.com/api/auth/session/victim.css`, we will find the same content as `/api/auth/session`, regardless of whether the victim.css file exists on the server.

*3. This way, the server’s web cache will see the “.css” extension and victim.css will be cached by the server with the victim’s session content*

*4. Now the hacker could simply go to* `https://chat.openai.com/api/auth/session/victim.css` and retrieve all of the victim’s authentication data.
<br>&nbsp;

----
## ***Credit***
Based on [Diego Tellaroli](https://medium.com/@diegotellaroli05/account-takeover-in-chatgpt-e134ed11654d)'s writeup.

----
## ***Support***
You can Follow [me](https://www.linkedin.com/in/bhavesh-pardhi-/) on LinkedIn or
<br><br>[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Support-orange?style=for-the-badge&logo=buy-me-a-coffee)](https://www.buymeacoffee.com/bhaveshpardhi)