[thm content discovery]


we can use curl to get http headers

curl website -v

when we understand the framework used we can refer to the documentation and gain knowledge how to bypass it

## identify technologies
use wappalyzer to identify technologies a website uses

we can get to know the framework used to create a website by checking its icons md5 hash in   https://wiki.owasp.org/index.php/OWASP_favicon_database owasp fav ico database


## get history
You can get the history of a website us the way back machine

## s3 bucket
always check site if they have an s3 bucket

## subdomain enumeration
Certificate Transparency (CT) logs used to validate sites ssl/tls 

http://crt.sh/
[https://transparencyreport.google.com/https/certificates](https://transparencyreport.google.com/https/certificates)

## dns bruteforce 
with dns recon tool

## osint domain

check domains with sublister


## fuzzing from virtual dns

```shell-session
ffuf -w /usr/share/wordlists/SecLists/Discovery/DNS/namelist.txt -H "Host: FUZZ.acmeitsupport.thm" -u http://10.10.113.127 -fs {size}
```

## scrape google data with
https://github.com/NikolaiT/GoogleScraper

run search strings then check its meta data


