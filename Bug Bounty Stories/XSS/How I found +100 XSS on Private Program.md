# ***How I found +100 XSS on Private Program 🧙‍♂️***

*1. Collecting all the domains that on scope.* <br>
*2. running Subfinder and assetfinder and combine the following subdomains in one list and remove duplicates*
```
subfinder -dL domains.txt -o subfider-subdomains.txt
cat domain_list.txt | assetfinder --subs-only > assetfinder-subdomains.txt
cat subfinder-subdomains.txt assetfinder-subdomains.txt > subdomains.txt
sort -u subdomains.txt > sort.txt
```
*3. we need to use Httpx to quickly and efficiently identify URLs that return a status code of 200 for a given domain list.*
```
cat sort.txt | httpx -mc 200 > 200_urls.txt
```
*4. Running Paramspider for crawling all the paramaters.*
```
for URL in $(</root/recon/target/200_urls.txt); do (python3 paramspider.py -d "${URL}");
done
```
*5. running KXSS for identifying the filtered , unfiltered Sympols note that Kxss scan could take several minutes or longer. Be patient and wait for the scan to complete*
```
cat filtered_urls.txt | kxss
```
<br>&nbsp;

----
## ***Credit***
Based on [jooelsaka](https://medium.com/@jooelsaka/how-i-found-100-reflected-cross-site-scripting-sql-injection-on-an-private-hackerone-bug-bounty-26eef05c9b63)'s writeup.

----
## ***Support***
You can Follow [me](https://www.linkedin.com/in/bhavesh-pardhi-/) on LinkedIn or
<br><br>[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Support-orange?style=for-the-badge&logo=buy-me-a-coffee)](https://www.buymeacoffee.com/bhaveshpardhi)
